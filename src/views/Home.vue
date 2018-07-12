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
        <p id="powered-by-slack">Powered by Slack</p>
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
  @include media('>=desktop') {
    grid-template-columns: 1fr 1fr;
  }
}

.main-title {
  text-align: center;
  color: $white;
  margin-left: 2rem;
  margin-bottom: 1rem;

  @include media('>=phone', '<=tablet') {
    font-size: 3rem;
    line-height: 4rem;
  }

  @include media('>=desktop') {
    text-align: left;
    font-size: 8rem;
    line-height: 7rem;
  }
}

.main-subtitle {
  text-align: center;
  color: $white;
  font-size: 2rem;
  margin-left: 2rem;

  @include media('>=desktop') {
    text-align: left;
    font-size: 4rem;
    line-height: 6rem;
  }
}

.heading {
  @include media('>=desktop') {
    margin-top: 6rem;
    margin-left: 4rem;
  }
}

.left-col {
  display: flex;
  flex-direction: column;
}

.right-col {
  display: flex;
  flex-direction: column;
  height: 100%;
  align-items: space-between;
}

#chat-window {
  width: 100%;
  // display: none;
  @include media('>=desktop') {
    width: 90%;
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

  @include media('>=desktop') {
    font-size: 2.5rem;
    height: 10rem;
    margin-left: 6rem;
    margin-top: 2rem;
    width: 40rem;
  }
}

.bold {
  font-weight: 700;
}

#nav {
  padding: 3rem;
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

#powered-by-slack {
  align-self: flex-end;
  color: $white;
  font-size: 2rem;
  margin-right: 2rem;
}
</style>
