<template>
  <div class="container">
    <div class="plus-list">
      <plus-item
          v-for="item in items"
          :key="item.id"
          :icon="item.icon"
          :title="item.title"
          :description="item.description"
      />
    </div>
  </div>
</template>

<script>
import PlusItem from "@/components/Card/PlusItem.vue";
import icon1 from "@/assets/advantages/icon1.png"
import icon2 from "@/assets/advantages/icon2.png"
import icon3 from "@/assets/advantages/icon3.png"
import icon4 from "@/assets/advantages/icon4.png"
import icon5 from "@/assets/advantages/icon5.png"
import icon6 from "@/assets/advantages/icon6.png"

export default {
  components: {
    PlusItem,
  },
  data() {
    return {
      items: [
        {
          id: 0,
          icon: icon1,
          title: "Уникальный дизайн",
          description: "Уникальный внешний вид благодаря дизайну с рисунком и возможностям персональной кастомизации",
        },
        {
          id: 1,
          icon: icon2,
          title: "Ультрамягкий",
          description: "Ультрамягкий подголовник наполненный пеной с эффектом памяти",
        },
        {
          id: 2,
          icon: icon3,
          title: "Максимальные регулировки",
          description: "Максимальный набор регулировок для удобства посадки",
        },
        {
          id: 3,
          icon: icon4,
          title: "Заточенность",
          description: "Заточенность под среднестатистического пользователя",
        },
        {
          id: 4,
          icon: icon5,
          title: "Быстрая сборка",
          description: "Рекордно быстрая скорость сборки",
        },
        {
          id: 5,
          icon: icon6,
          title: "Высокое качество",
          description: "Высокое качество материалов и изготовления",
        },
      ],
    };
  },

}
</script>

<style lang="scss" scoped>
.container {
  display: flex; /* Добавляем flex контейнер */
  justify-content: center; /* Центрируем по горизонтали */
  align-items: center; /* Центрируем по вертикали */
  width: 100%; /* Или любая фиксированная ширина, которая позволяет центрировать */
  height: 100vh;
  //background-color: #ffffff;
  background-image: url("@/assets/chairs/fon-chairs.svg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  border-radius: 30px;

}
.plus-list {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  width: 1000px;
  margin: 0 auto; /* Центрирует сетку по горизонтали */


}


</style>