<template>
  <div class="full-screen-block">
    <div class="text-container">
      <p>Текст слева</p>
    </div>
    <div class="image-container">
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

.text-container {
  flex: 1;
  padding: 20px;
  text-align: left;
}

.image-container {
  flex: 1;
  padding: 20px;
  text-align: right;
}

img {

  height: auto;
}
</style>