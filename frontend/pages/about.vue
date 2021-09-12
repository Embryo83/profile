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
    <p class="description">
      Письменный переводчик(художественный перевод), автор-исполнитель,
      веб-разработчик
    </p>
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

<style scoped>
.container {
  flex-direction: column;
  justify-content: center;
  align-items: center;
  display: flex;
  text-align: center;
}

.title {
  padding: 10px;
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
