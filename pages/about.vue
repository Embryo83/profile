<template>
  <div class="container">
    <div class="main__links">
      <NLink class="main__button" to="/">Главная</NLink>
      <button class="main__button main__button--type--active" to="/about">
        Обо мне
      </button>
      <NLink class="main__button" to="/contacts">Контакты</NLink>
    </div>
    <h2 class="title">Обо мне</h2>
    <div v-if="error">
      {{ error }}
    </div>
    <div v-else>
    <p v-for="profile in profiles" :key="profile.id" class="description">
      {{ profile.about }}
    </p>
    </div>
    <iframe
      frameborder="0"
      style="border: none; width: 100%; height: 180px"
      width="100%"
      height="180"
      src="https://music.yandex.ru/iframe/#track/84509010/16027957"
      >Слушайте
      <a href="https://music.yandex.ru/album/16027957/track/84509010"
        >Никотин</a
      >
      — <a href="https://music.yandex.ru/artist/5116202">Andrej Rusty</a> на
      Яндекс.Музыке</iframe
    >
  </div>
</template>

<script>
export default {
  data () {
    return {
      profiles: [],
      error: null
    }
  },
  async mounted () {
    try {
      this.profiles = await this.$strapi.$profiles.find()
    } catch (error) {
      this.error = error
    }
  },
}
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
  font-size: 1rem;
  line-height: 1.5;
  width: 90vw;
  text-align: center;
  margin-bottom: 10px;
}
</style>
