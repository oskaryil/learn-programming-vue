<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Lato");

html {
  font-size: 62.5%;
  height: 100%;
}

body {
  padding: 0;
  margin: 0;
  font-family: "Roboto", sans-serif;
  height: 100%;
}

h1,
h2,
h3,
h4,
h5 {
  margin: 0;
  padding: 0;
}

#app {
  font-family: "Roboto", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
