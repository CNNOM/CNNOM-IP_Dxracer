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
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100vh;
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
  margin: 0 auto;
}

@media (max-width: 768px) {
  .container{
    height: auto;
    background-repeat: repeat;

  }
  .plus-list {
    grid-template-columns: 1fr;
    display: flex; /* Изменяем grid на flex для простоты центрирования */
    flex-direction: column; /* Изменяем направление на столбец для мобильных устройств */
    justify-content: center; /* Центрируем элементы по горизонтали */
    align-items: center; /* Центрируем элементы по вертикали */
    width: 90vw;
  }
}

@media (min-width: 769px) and (max-width: 1024px) {
  .plus-list {
    grid-template-columns: repeat(2, 1fr);
    width: 80vw;
  }
}

@media (min-width: 1025px) and (max-width: 1280px) {
  .plus-list {
    grid-template-columns: repeat(2, 1fr);
    width: 70vw;
  }
}

@media (min-width: 1281px) and (max-width: 1920px) {
  .plus-list {
    grid-template-columns: repeat(2, 1fr);
    width: 60vw;
  }
}

</style>