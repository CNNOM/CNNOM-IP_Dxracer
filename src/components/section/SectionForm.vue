<template>
<div class="container">
  <div class="modal-content">
    <h2>Оформление заказа</h2>
    <form @submit.prevent="submitForm">
      <form-group id="firstName" label="Имя" v-model="form.firstName" required></form-group>
      <form-group id="lastName" label="Фамилия" v-model="form.lastName" required></form-group>
      <form-group id="phone" label="Телефон" type="tel" v-model="form.phone" required></form-group>
      <form-group id="email" label="Email" type="email" v-model="form.email" required></form-group>
      <form-group id="city" label="Город" v-model="form.city" required></form-group>
      <button type="submit">Отправить</button>
    </form>
  </div>
</div>
</template>

<script>
import FormGroup from "@/components/form/FormGroup.vue";

export default {
  components: {FormGroup},
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
  },
  props: {
    showModal: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    submitForm() {
      console.log(this.form);
      this.resetForm();
    },
    resetForm() {
      this.form.firstName = ' ';
      this.form.lastName = ' ';
      this.form.phone = ' ';
      this.form.email = ' ';
      this.form.city = ' ';
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url("@/assets/5.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  padding: 10% 5%;
}
.modal {
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-content {
  background: white;
  width: 500px;
  padding: 20px;
  border-radius: 5px;
  position: relative;
}

.close {
  position: absolute;
  top: 10px;
  right: 15px;
  font-size: 28px;
  cursor: pointer;
}

button[type="submit"] {
  display: block;
  width: 100%;
  padding: 10px;
  background-color: rgba(255, 255, 255, 0.5);
  border: 3px solid gold;
  color: gold;
  cursor: pointer;
  font-size: 1.2rem;
  border-radius: 15px ;

}

button[type="submit"]:hover {
  background-color: gold;
  color: white;
}
</style>