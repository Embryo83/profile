<template>
  <div class="container">
    <div class="main__links">
      <NLink class="main__button" to="/">Главная</NLink>
      <NLink class="main__button" to="/about">Обо мне</NLink>
      <button class="main__button main__button--type--active" to="/contacts">
        Контакты
      </button>
    </div>
    <h2 class="title">Контакты</h2>
    <Contacts />
  </div>
</template>

<script>
import Contacts from "~/components/Contacts.vue";

export default {
  components: {
    Contacts,
  },
};
</script>

<style scoped>
.container {
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  display: flex;
  text-align: center;
}

.title {
  padding: 50px;
  text-transform: uppercase;
  color: #fff;
}

.description {
  width: 90vw;
  font-size: 1rem;
  line-height: 1.5;
  text-align: center;
  margin-bottom: 10px;
}
</style>
