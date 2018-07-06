<template>
  <div class="home">
    <div class="left-col">
      <div class="heading">
        <h1 class="main-title">Learn <br>programming</h1>
        <h2 class="main-subtitle">a community driven by learning.</h2>
      </div>
      <button id="cta-btn">Join <span class="bold">150</span> members now</button>
    </div>
    <div class="right-col">
      <nav id="nav">
        <router-link to="/about">About</router-link>
      </nav>
      <img id="chat-window" src="../assets/chat_window.png" alt="slack chat window" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'home',
  components: {}
};
</script>

<style lang="scss">
$purple: #6a5acd;
$white: #fff;
$btn-green: #66bb42;

.home {
  width: 100%;
  min-height: 100%;
  height: 100vh;
  background-color: $purple;
  display: grid;
  grid-template-columns: 1fr;
}

@media (min-width: 900px) {
  .home {
    grid-template-columns: 1fr 1fr;
  }
}

.main-title {
  text-align: left;
  color: $white;
  font-size: 5rem;
  margin-left: 2rem;
  line-height: 5.5rem;
  margin-bottom: 1rem;
}

.main-subtitle {
  text-align: left;
  color: $white;
  font-size: 2rem;
  margin-left: 2rem;
}

.heading {
  margin-top: 8rem;
}

.left-col {
  display: flex;
  flex-direction: column;
}

.right-col {
}

#chat-window {
  width: 200px;
  @media (min-width: 900px) {
    width: 80%;
  }
}

#cta-btn {
  background-color: $btn-green;
  outline: none;
  border: 0;
  color: $white;
  height: 6rem;
  width: 30rem;
  font-size: 1.75rem;
  border-radius: 10rem;
  margin-left: 2rem;
  margin-top: 5rem;
}

.bold {
  font-weight: 700;
}

#nav {
  padding: 30px;
  font-weight: bold;
  text-align: right;
  margin-right: 2rem;
  a {
    color: $white;
    font-size: 2rem;
    text-decoration: none;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
