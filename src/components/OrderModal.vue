<template>
  <div v-if="showModal" class="modal">
    <div class="modal-content">
      <span class="close" @click="closeModal">&times;</span>
      <h2>Оформление заказа</h2>
      <form @submit.prevent="submitForm">
        <div class="form-group">
          <label for="firstName">Имя</label>
          <input type="text" id="firstName" v-model="form.firstName" required>
        </div>
        <div class="form-group">
          <label for="lastName">Фамилия</label>
          <input type="text" id="lastName" v-model="form.lastName" required>
        </div>
        <div class="form-group">
          <label for="phone">Телефон</label>
          <input type="tel" id="phone" v-model="form.phone" required>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="form.email" required>
        </div>
        <div class="form-group">
          <label for="city">Город</label>
          <input type="text" id="city" v-model="form.city" required>
        </div>
        <button type="submit">Отправить</button>
      </form>
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
  },
  props: {
    showModal: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    closeModal() {
      this.$emit('update:showModal', false);
    },
    submitForm() {
      console.log(this.form);
      this.closeModal();
    }
  }
}
</script>

<style lang="scss" scoped>
.modal {
  position: fixed;
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

.form-group {
  margin-bottom: 15px;
  margin-right: 20px;
}

.form-group label {
  display: block;
  margin-bottom: 5px;
}

.form-group input {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
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