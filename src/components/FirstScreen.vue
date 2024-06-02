<template>
  <header class="page-header">
    <div class="full-screen-block">
      <div class="text-container slide-up">
        <img src="@/assets/DXRacer_Primary_Black_Logo.png">
        <h1>DXRACER CRA/D5000</h1>
        <p>- геймерское кресло Craft Originals,
          обитое классической черной эко-кожей с изящной золотой прострочкой.</p>
        <button class="golden-button"  @click="showModal = true">Оформить заказ</button>
      </div>
      <div class="image-container slide-up">
        <img src="@/assets/D5000N-002.2560.png" alt="Изображение справа">
      </div>
    </div>
    <order-modal v-model:showModal="showModal" />

  </header>
</template>

<script>
import OrderModal from '@/components/OrderModal.vue'
export default {
  components: {
    OrderModal,
  },
  data() {
    return {
      showModal: false
    };
  }

};
</script>

<style lang="scss" scoped>

.page-header {
  font-family: Noto Sans, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  //background-color: #4a4a4a;
}

.full-screen-block {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 5vh 5vw; /* Отступы сверху и снизу 5vh, по бокам 5vw */
  width: 100%;
  max-width: 1600px; /* Максимальная ширина блока */
  height: 100%;
  max-height: 700px;
  background: url("@/assets/fon-header.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  overflow: hidden;
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.3); /* Внутренняя тень */
  border-radius: 30px;
}

.text-container,
.image-container {
  flex: 1;
  padding: 20px;
  text-align: center;
  opacity: 0; /* Делаем элементы невидимыми изначально */
  transform: translateY(20px); /* Сдвигаем элементы вниз */
  transition: all 1s ease-in-out; /* Добавляем плавную анимацию */
}

.slide-up {
  animation: slideUp 1.5s forwards; /* Запускаем анимацию */
}

@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(50vh);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
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

.image-container::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100%;
  //background: purple;
  border: 3px solid #ffd700;
  transform: skewY(-30deg);
  z-index: -1;
  border-radius: 50%;
}
.text-container,
.image-container {
  flex: 1;
  padding: 20px;
  text-align: center;
  opacity: 0;
  transform: translateY(20px);
  transition: all 1s ease-in-out;
}

img {
  max-width: 100%;
  height: auto;
}

@media screen and (max-width: 1920px) {
  .full-screen-block {
    padding: 5vh 5vw; /* Отступы сверху и снизу 5vh, по бокам 5vw */
  }
}

@media screen and (max-width: 1600px) {
  .full-screen-block {
    padding: 4vh 4vw; /* Отступы сверху и снизу 4vh, по бокам 4vw */
  }
}

@media screen and (max-width: 1280px) {
  .full-screen-block {
    padding: 3vh 3vw; /* Отступы сверху и снизу 3vh, по бокам 3vw */
  }
}

@media screen and (max-width: 1024px) {
  .full-screen-block {
    padding: 2vh 2vw; /* Отступы сверху и снизу 2vh, по бокам 2vw */
  }
}

@media screen and (max-width: 768px) {
  .full-screen-block {
    padding: 1vh 1vw; /* Отступы сверху и снизу 1vh, по бокам 1vw */
  }
}

@media screen and (max-width: 480px) {
  .full-screen-block {
    padding: 0.5vh 0.5vw; /* Отступы сверху и снизу 0.5vh, по бокам 0.5vw */
  }
}

@media screen and (max-width: 320px) {
  .full-screen-block {
    padding: 0.5vh 0.5vw; /* Отступы сверху и снизу 0.5vh, по бокам 0.5vw */
  }
}


</style>