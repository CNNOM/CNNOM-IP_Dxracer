<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-md-6">
        <form>
          <div class="form-group">
            <label for="firstName">Имя</label>
            <input type="text" class="form-control" id="firstName" v-model="form.firstName">
          </div>
          <div class="form-group">
            <label for="lastName">Фамилия</label>
            <input type="text" class="form-control" id="lastName" v-model="form.lastName">
          </div>
          <div class="form-group">
            <label for="phone">Телефон</label>
            <input type="tel" class="form-control" id="phone" v-model="form.phone">
          </div>
          <div class="form-group">
            <label for="email">Email</label>
            <input type="email" class="form-control" id="email" v-model="form.email">
          </div>
          <div class="form-group">
            <label for="city">Город</label>
            <input type="text" class="form-control" id="city" v-model="form.city">
          </div>
          <button type="submit" class="btn btn-primary">Отправить</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        firstName: '',
        lastName: '',
        phone: '',
        email: '',
        city: ''
      }
    };
  }
}
</script>

<style lang="scss" scoped>
.container {
  margin-top: 50px;
}
</style>