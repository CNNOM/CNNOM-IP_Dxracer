<template>
  <div class="full-screen-container">
    <div class="container">
      <div class="image-container">
        <img src="@/assets/information/img1.jpg" alt="Картинка справа">
      </div>
      <div class="text-container">
        <h2>КРЕСЛА DXRACER CRAFT </h2>
        <p>Серия Craft от DXRacer – это линейка уникальных кресел, каждое из которых имеет свой собственный дизайн. Их отличительной особенностью является нанесение на обивку из мягкой эко-кожи необычных рисунков по технологии трехмерной вышивки.</p>
        <p>Спинка кресел данной серии имеет угол наклона до 150 градусов, качание кресла осуществляется при помощи механизма мультиблок, а подлокотники обладают 4D-регулировкой. Также в спинку встроена регулируемая поясничная опора, способствующая сохранению осанки.</p>
        <p>В качестве наполнителя для подушки-подголовника используется мягкая пена и охлаждающий гель.</p>
        <p>Помимо всего прочего, в названии серии есть особый смысл. Ведь вы можете кастомизировать кресло по своему вкусу, заказав нанесение собственного изображения и свою уникальную расцветку.</p>
        <h4>DxRacer Craft – скрафть свое кресло сам!</h4>
        <button class="golden-button"  @click="showModal = true">Оформить заказ</button>
      </div>
    </div>
  </div>

  <order-modal v-model:showModal="showModal" />
</template>

<script>
import OrderModal from "@/components/OrderModal.vue";

export default {
  components: {OrderModal},
  data() {
    return {
      showModal: false
    };
  }
}
</script>

<style lang="scss" scoped>
.full-screen-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100vw;
}
.container{
  width: 70vw;
  display: flex;
  justify-content: center;
  align-items: center;
}

.text-container {
  text-align: center; /* Выравнивание текста по левому краю */
  flex: 1;
  padding-left: 50px;

}

.image-container img {
  max-height: 100%;
  max-width: 100%;
}
img {
  max-width: 100%;
  height: auto;
  border: 2px solid #ffc400;
  border-radius: 30px;
}
p{
  text-align: left; /* Выравнивание текста по левому краю */

}

.golden-button {
  background-color: rgba(255, 255, 255, 0.5);
  border: 3px solid gold;
  color: gold;
  padding: 10px 20px;
  margin-top: 20px;
  cursor: pointer;
  font-size: 1.5rem;
  transition: background-color 0.3s ease, color 0.3s ease;
  border-radius: 15px ;
}

.golden-button:hover {
  background-color: gold;
  color: white;
}

</style>