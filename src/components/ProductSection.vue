<template>
  <div class="image-switcher">
    <h1>
      ddddddddddddd
    </h1>
    <div class="main-image">
      <p>{{selectedImage}}</p>
      <img :src="selectedImage" alt="Selected Image">
    </div>
    <div class="color-switcher">
      <div
          v-for="(color, index) in Object.values(colors)"
          :key="index"
          :style="{ backgroundColor: color }"
          @click="changeImage(index)"
          class="color-block"
      ></div>
    </div>
  </div>
</template>

<script>
import blackBlue from '@/assets/chairs/black-blue.jpg';
import blackChina from '@/assets/chairs/black-china.jpg';
import USA from '@/assets/chairs/USA.jpg';
import pink from '@/assets/chairs/pink.jpg';
import white from '@/assets/chairs/white.jpg';
import blackGold from '@/assets/chairs/black-gold.jpg';
import greyYellow from '@/assets/chairs/grey-yellow.jpg';
import yellow from '@/assets/chairs/yellow.jpg';


export default {
  data() {
    return {
      selectedImage: '',
      colors: {
        0: '#000000',
        1: '#ffc400',
        2: '#ff0000',
        3: '#e600ff',
        4: '#ffffff',
        5: '#48fff0',
        6: '#6c6c61',
        7: '#deff00',
      },
      images: {
        0: blackGold,
        1: blackChina,
        2: USA,
        3: pink,
        4: white,
        5: blackBlue,
        6: greyYellow,
        7: yellow,
      }
    };
  },
  methods: {
    changeImage(index) {
      this.selectedImage = this.images[index];
      console.log(this.selectedImage)
    },
  },
  mounted() {
    // Установка изображения по умолчанию при монтировании компонента
    this.selectedImage = this.images[0];
  },
}
</script>

<style lang="scss" scoped>
.image-switcher {
  text-align: center;
  padding: 20px;
}

.main-image {
  margin-bottom: 20px;
}

.main-image img {
  max-width: 100%;
  height: auto;
}

.color-switcher {
  display: flex;
  justify-content: center;
}

.color-block {
  border: 1px solid rgba(0, 0, 0, 0.35);

  width: 50px;
  height: 50px;
  margin: 5px;
  border-radius: 50%;
  cursor: pointer;
}
</style>