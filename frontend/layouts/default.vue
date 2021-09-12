<template>
  <div class="container">
    <Nuxt />
  </div>
</template>

<style>
html {
  box-sizing: border-box;
  font-family: Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  color: #fff;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.container {
  justify-content: center;
  align-items: center;
  display: flex;
  min-height: 100vh;
  text-align: center;
  background: #014;
}

.main__button {
  display: inline-block;
  padding: 10px 30px;
  font-weight: 900;
  text-decoration: none;
  color: #aca;
  border: 5px solid #aca;
  border-radius: 15px;
  cursor: pointer;
}

.main__button:hover {
  color: #fff;
  background-color: #aca;
}

.main__button--type--active {
  color: #fff;
  border: 8px solid #aca;
  background-color: #aca;
}

.main__button--type--back {
  display: inline-block;
  padding: 10px 30px;
  text-decoration: none;
  color: #245;
  border: 5px solid #245;
  border-radius: 15px;
  margin-left: 15px;
}

.main__button--type--back:hover {
  color: #fff;
  background-color: #245;
}
</style>
