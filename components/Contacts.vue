<template>
  <div class="contacts">
    <ul class="contacts__items contacts__items--type--left">
      <li class="contacts__item">Email</li>
      <li class="contacts__item">Telegram</li>
      <li class="contacts__item">Instagram</li>
      <li class="contacts__item">VK</li>
    </ul>
    <div v-if="error">
      {{ error }}
    </div>
    <div v-else>
    <ul v-for="profile in profiles" :key="profile.id" class="contacts__items contacts__items--type--right">
      <li class="contacts__item">
        <a href="mailto:andrejrusty@icloud.com" class="contacts__link"
          >{{ profile.email }}</a
        >
      </li>
      <li class="contacts__item">
        <a href="https://t.me/andrej_rusty" class="contacts__link"
          >{{ profile.telegram }}</a
        >
      </li>
      <li class="contacts__item">
        <a href="https://instagram.com/andrejrusty" class="contacts__link"
          >{{ profile.instagram }}</a
        >
      </li>
      <li class="contacts__item">
        <a href="https://vk.com/rastegaev" class="contacts__link"
          >{{ profile.vk }}</a
        >
      </li>
    </ul>
    </div>
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
.contacts {
  display: flex;
  padding: 10px;
}

.contacts__items {
  list-style: none;
}

.contacts__items--type--left {
  font-weight: 900;
  letter-spacing: 5px;
  text-align: right;
}

.contacts__items--type--right {
  line-height: 1.45;
  letter-spacing: 1px;
  text-align: left;
}

.contacts__link {
  text-decoration: none;
  color: #fff;
}

.contacts__link:hover {
  color: #42c;
  opacity: 0.8;
}
</style>
