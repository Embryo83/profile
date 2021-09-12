<template>
  <div>
    <div class="main__links">
      <button class="main__button main__button--type--active">Главная</button>
      <NLink class="main__button" to="/about">Обо мне</NLink>
      <NLink class="main__button" to="/contacts">Контакты</NLink>
    </div>
    <div v-if="error">
      {{ error }}
    </div>
    <div v-else>
    <h1 v-for="profile in profiles" :key="profile.id" class="main__title">
      {{ profile.name }} <span class="main__title--type--surname">{{ profile.surname }}</span>
    </h1>
    </div>
    <Photo />
  </div>
</template>

<script>
import Photo from "~/components/Photo.vue";

export default {
  components: {
    Photo,
  },
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

.main__title {
  padding: 50px;
}

.main__title--type--surname {
  text-transform: uppercase;
}
</style>
