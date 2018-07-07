<template>
  <div class="wrapper">
    <div class="nav">
      <nav id="nav">
        <router-link to="/about">About</router-link>
      </nav>
    </div>
    <div class="two-columns">
      <div class="left-col">
        <div class="heading">
          <h1 class="main-title">Learn <br>programming</h1>
          <h2 class="main-subtitle">a community driven by learning.</h2>
        </div>
        <button id="cta-btn">Join <span class="bold">150</span> members now</button>
      </div>
      <div class="right-col">
        <img id="chat-window" src="../assets/chat_window.png" alt="slack chat window" />
      </div>
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
@import '../assets/_include-media.scss';
$purple: #6a5acd;
$white: #fff;
$btn-green: #66bb42;

$breakpoints: (
  phone: 320px,
  tablet: 768px,
  desktop: 1024px
);

.wrapper {
  width: 100%;
  min-height: 100vh;
  height: 100%;
  background-color: $purple;
  // grid-auto-rows: auto;
  // grid-gap: 2rem;
  @media (min-width: 900px) {
    height: 100vh;
  }
}

.nav {
  display: grid;
  grid-template-columns: 1fr;
}

.two-columns {
  display: grid;
  grid-template-columns: 1fr;
  // grid-auto-rows: auto;
  // grid-gap: 2rem;
  grid-template-rows: 1fr;
  grid-row-gap: 1rem;
  @media (min-width: 900px) {
    grid-template-columns: 1fr 1fr;
    height: 100vh;
  }
}

.main-title {
  text-align: center;
  color: $white;
  font-size: 5rem;
  margin-left: 2rem;
  line-height: 5.5rem;
  margin-bottom: 1rem;

  @include media('>=phone', '<=tablet') {
    font-size: 3rem;
    line-height: 4rem;
  }

  @media (min-width: 900px) {
    text-align: left;
  }
}

.main-subtitle {
  text-align: center;
  color: $white;
  font-size: 2rem;
  margin-left: 2rem;

  @media (min-width: 900px) {
    text-align: left;
  }
}

.heading {
}

.left-col {
  display: flex;
  flex-direction: column;
}

.right-col {
}

#chat-window {
  width: 100%;
  // display: none;
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
  margin: 0 auto;
  margin-top: 2rem;

  @media (min-width: 900px) {
    margin-left: 2rem;
  }
}

.bold {
  font-weight: 700;
}

#nav {
  padding: 30px;
  font-weight: bold;
  text-align: right;
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
