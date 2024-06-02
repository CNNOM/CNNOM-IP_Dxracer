<template>
  <div>
    <first-screen ref="firstScreen"/>
    <information-section ref="informationSection"/>
    <advantages-section ref="advantagesSection"/>
  </div>
</template>

<script>
import FirstScreen from '@/components/FirstScreen.vue'
import AdvantagesSection from "@/components/AdvantagesSection.vue";
import InformationSection from "@/components/InformationSection.vue";

export default {
  components: {FirstScreen, AdvantagesSection, InformationSection},
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      const firstScreen = this.$refs.firstScreen.$el;
      const informationSection = this.$refs.informationSection.$el;
      const advantagesSection = this.$refs.advantagesSection.$el;

      if (window.innerHeight + window.scrollY >= firstScreen.offsetTop + firstScreen.offsetHeight && window.scrollY < informationSection.offsetTop) {
        window.scrollTo(0, informationSection.offsetTop);
      } else if (window.innerHeight + window.scrollY >= informationSection.offsetTop + informationSection.offsetHeight && window.scrollY < advantagesSection.offsetTop) {
        window.scrollTo(0, advantagesSection.offsetTop);
      }
    }
  }

}
</script>

<style lang="scss" scoped>
.full-page-container {
  scroll-snap-type: y mandatory;
  overflow-y: scroll;
  height: 100vh;
}

.section {
  scroll-snap-align: start;
  height: 100vh;
}
</style>