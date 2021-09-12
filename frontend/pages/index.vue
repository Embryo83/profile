<template>
  <div>
    <div class="main__links">
      <button class="main__button main__button--type--active">Главная</button>
      <NLink class="main__button" to="/about">Обо мне</NLink>
      <NLink class="main__button" to="/contacts">Контакты</NLink>
    </div>
    <h1 class="main__title">
      Андрей <span class="main__title--type--surname">Растегаев</span>
    </h1>
    <Photo />
  </div>
</template>

<script>
import Photo from "~/components/Photo.vue";

export default {
  components: {
    Photo,
  },
}
</script>

<style scoped>
.main__title {
  padding: 10px;
}

.main__title--type--surname {
  text-transform: uppercase;
}
</style>
