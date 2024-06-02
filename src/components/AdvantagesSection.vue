<template>
  <div class="plus-list">
    <div class="plus-item">
      <img src="@/assets/advantages/icon1.png" alt="Icon 1" class="plus-icon">
      <h2>Уникальный дизайн</h2>
      <p>Уникальный внешний вид благодаря дизайну с рисунком и возможностям персональной кастомизации</p>
    </div>
    <div class="plus-item">
      <img src="@/assets/advantages/icon2.png" alt="Icon 2" class="plus-icon">
      <h2>Ультрамягкий</h2>
      <p>Ультрамягкий подголовник наполненный пеной с эффектом памяти</p>
    </div>
    <div class="plus-item">
      <img src="@/assets/advantages/icon3.png" alt="Icon 3" class="plus-icon">
      <h2>Максимальные регулировки</h2>
      <p>Максимальный набор регулировок для удобства посадки</p>
    </div>
    <div class="plus-item">
      <img src="@/assets/advantages/icon4.png" alt="Icon 4" class="plus-icon">
      <h2>Заточенность</h2>
      <p>Заточенность под среднестатистического пользователя</p>
    </div>
    <div class="plus-item">
      <img src="@/assets/advantages/icon5.png" alt="Icon 5" class="plus-icon">
      <h2>Быстрая сборка</h2>
      <p>Рекордно быстрая скорость сборки</p>
    </div>
    <div class="plus-item">
      <img src="@/assets/advantages/icon6.png" alt="Icon 5" class="plus-icon">
      <h2>Высокое качество</h2>
      <p>Высокое качество материалов и изготовления</p>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.plus-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.plus-item {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.plus-icon {
  width: 2rem;
  height: 2rem;
}

.plus-item h2 {
  font-size: 1.5rem;
  color: #333;
}

.plus-item p {
  font-size: 1rem;
  color: #666;
}
</style>