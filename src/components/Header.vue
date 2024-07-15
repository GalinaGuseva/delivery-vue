<template>
  <header class="header">
        <div class="container">
          <div class="header-box">
            <router-link to="/" class="header-logo logo">
              <img src="../assets/img/logo.png" alt="logo" />
            </router-link>
            <div class="header-controls">
              <button class="btn btn-primary">
                <img src="../assets/img/icons/user.png" alt="user" />
                Войти
              </button>
              <button class="btn btn-outline" @click="openModal()">
                <img src="../assets/img/icons/shopping-cart.png" alt="корзина" />
                Корзина
              </button>
            </div>
          </div>
        </div>
      </header>
</template>

<script setup>
const emit = defineEmits(['toggleModal'])
const openModal = () => emit('toggleModal');

</script>

<style scoped>
.header {
  min-height: 124px;
  display: flex;
  align-items: center;
}

.header-box {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header-controls {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 10px;
}

.logo {
  max-width: 100px;
}

.logo img {
  width: 100%;
}

.btn {
  display: flex;
  padding: 8px 16px;
  align-items: center;
  gap: 4px;
  border-radius: 2px;
  outline: none;
  cursor: pointer;
}

.btn-primary {
  background: #1890ff;
  border: 1px solid #1890ff;
  color: #fff;
}

.btn-outline {
  border: 1px solid #d9d9d9;
  background: #fff;
  box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0);
  color: #595959;
}
</style>