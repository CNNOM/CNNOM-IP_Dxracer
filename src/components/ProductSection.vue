<template>
  <div class="container">
    <div class="text-blocks">
      <h1>Компьютерное кресло {{this.nameChairs}}</h1>
    </div>
    <div class="image-switcher">
      <h1>Our chairs</h1>
      <div class="main-image">
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
    <div class="text-blocks">
      <div v-for="(text, index) in textBlocksRight" :key="index" class="text-block">
        <p>{{ text }}</p>
      </div>
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
      nameChairs: '',
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
      },
      nameChairsId: {
        0:'DXRacer Craft CRA/D5000/N Originals',
        1:'DXRacer Craft CRA/D5000/NC1 Koi Fish',
        2:'DXRacer Craft CRA/D5000/BW America Edition',
        3:'DXRacer Craft CRA/D5000/P Hello Human Cat',
        4:'DXRacer Craft CRA/D5000/W Thinker',
        5:'DXRacer Craft CRA/D5000/NC9 Guild Wars 2: End of Dragons Edition' ,
        6:'DXRacer Craft CRA/D5000/GY Astronaut',
        7:'DXRacer Craft CRA/D5000/YW Rabbit in Dino'
      },
      textBlocksRight: [
        'Компьютерное кресло DXRacer Craft CRA/D5000/YW Rabbit in Dino – кресло новой серии DXRAcer, созданных на базе серии Drifting.',
        'Кресло DXRacer Craft CRA/D5000/YW выполнено из Эко-кожи яркого желтого цвета с вышитым изображением пушистого кролика. Но это только с одной стороны.',
        'С другой же стороны это уже совсем не милый кролик, а свирепый Дракон готовый к подвигам! Желтое кресло DXRacer Rabbit in Dino многих порадует своим оригинальным рисунком и яркой расцветкой.'
      ]
    };
  },
  methods: {
    changeImage(index) {
      this.selectedImage = this.images[index];
      this.nameChairs = this.nameChairsId[index];
      console.log(this.selectedImage)
      console.log(this.nameChairs)
    },
  },
  mounted() {
    // Установка изображения по умолчанию при монтировании компонента
    this.nameChairs = this.nameChairsId[0];
    this.selectedImage = this.images[0];
  },
}
</script>

<style lang="scss" scoped>
.container {
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column; /* Изменение направления flex на столбец для мобильных устройств */
  justify-content: center;
  align-items: center;
}

.image-switcher {
  text-align: center;
  padding: 20px;
}

.main-image {
  margin-bottom: 20px;
}

.main-image img {
  max-width: 70vw;
  height: auto; /* Изменение высоты на автоматическую для сохранения пропорций */
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

.text-blocks {
  text-align: center;
  margin: 5vw;
  width: 100%; /* Изменение ширины на 100% для адаптации */
}

.text-block {
  flex: 1;
  margin: 10px;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 5px;
}

@media (max-width: 479px) {
  .container {
    height: auto;
  }
  .text-blocks {
    width: 80%; /* Возвращаем ширину блоков текста для планшетов и более крупных устройств */
  }
  .color-block{
    width: 30px;
    height: 30px;
  }
}

@media (min-width: 480px) and (max-width: 767px) {
  .container {
    height: auto;
  }
  .text-blocks {
    width: 80%; /* Возвращаем ширину блоков текста для планшетов и более крупных устройств */
  }
  .color-block{
    width: 40px;
    height: 40px;
  }
}

@media (min-width: 768px) {

  .container {
    height: auto;
  }
  .text-blocks {
    width: 80%; /* Возвращаем ширину блоков текста для планшетов и более крупных устройств */
  }

}

@media (min-width: 1024px)  and (max-width: 1280px) {
  .container {
    height: auto;
  }
  .main-image img {
    max-width: 50vw; /* Уменьшаем максимальную ширину изображения для более крупных экранов */
  }
}

@media (min-width: 1280px) and (max-width: 1920px) {
  .container {
    height: 100vh;
    flex-direction: row; /* Изменение направления flex на столбец для мобильных устройств */

  }
  .main-image img {
    max-width: 40vw; /* Уменьшаем максимальную ширину изображения для еще более крупных экранов */
  }
}

@media (min-width: 1920px) {
  .container {
    height: 100vh;
    flex-direction: row; /* Изменение направления flex на столбец для мобильных устройств */
  }

  .main-image img {
    max-width: 30vw; /* Уменьшаем максимальную ширину изображения для самых крупных экранов */
  }
}
</style>