<template>
  <div class="plus-item">
    <img :src="icon"  class="plus-icon" alt="">
    <div class="plus-text">
      <h2>{{ title }}</h2>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    }
  },
}
</script>

<style lang="scss" scoped>
.plus-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  width: 500px;
  margin-top: 3rem;
}

.plus-icon {
  width: 50px;
  height: 50px;
  margin-bottom: 1rem;
}
.plus-text{
  border: 2px solid black;
  border-radius: 10px;
}
.plus-item h2 {
  font-size: 1.2rem;
  color: #333;
  margin-bottom: 0.4rem;
  padding: 4px;
}

.plus-item p {
  font-size: 0.9rem;
  color: #666;
  width: 300px;
}

@media (max-width: 768px) {
  .plus-item{
    width: auto;
  }
}
</style>