<template>
  <div class="full-screen-block">
    <div class="text-container slide-up">
      <p>Текст слева</p>
    </div>
    <div class="image-container slide-up">
      <img src="@/assets/logo.svg" alt="Изображение справа">
    </div>
  </div>
</template>

<script>
export default {

};
</script>

<style lang="scss" scoped>
.full-screen-block {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100vh;
  width: 100vw;
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
  animation: slideUp 2s forwards; /* Запускаем анимацию */
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

img {
  max-width: 70%;
  height: auto;
}
</style>