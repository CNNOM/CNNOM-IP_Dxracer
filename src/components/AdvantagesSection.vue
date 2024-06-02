<template>
  <div class="container">
    <div class="plus-list">
      <plus-item
          icon="@/assets/advantages/icon1.png"
          title="Уникальный дизайн"
          description="Уникальный внешний вид благодаря дизайну с рисунком и возможностям персональной кастомизации"
      />
      <plus-item
          icon="@/assets/advantages/icon2.png"
          title="Ультрамягкий"
          description="Ультрамягкий подголовник наполненный пеной с эффектом памяти"
      />
      <plus-item
        icon="@/assets/advantages/icon3.png"
        title="Максимальные регулировки"
        description="Максимальный набор регулировок для удобства посадки"
      />
      <plus-item
          icon="@/assets/advantages/icon4.png"
          title="Заточенность"
          description="Заточенность под среднестатистического пользователя"
      />
      <plus-item
          icon="@/assets/advantages/icon5.png"
          title="Быстрая сборка"
          description="Рекордно быстрая скорость сборки"
      />
      <plus-item
          icon="@/assets/advantages/icon6.png"
          title="Высокое качество"
          description="Высокое качество материалов и изготовления"
      />
    </div>
  </div>
</template>

<script>
import PlusItem from "@/components/Card/PlusItem.vue";

export default {
  components: {
    PlusItem,
  }

}
</script>

<style lang="scss" scoped>
.container {
  display: flex; /* Добавляем flex контейнер */
  justify-content: center; /* Центрируем по горизонтали */
  align-items: center; /* Центрируем по вертикали */
  width: 100%; /* Или любая фиксированная ширина, которая позволяет центрировать */
  height: 100vh;
  background-color: #ffffff;
}
.plus-list {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  width: 1000px;
  margin: 0 auto; /* Центрирует сетку по горизонтали */
}


</style>