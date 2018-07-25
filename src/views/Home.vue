<template>
  <div class="wrapper">
    <div class="nav">
      <nav id="nav">
        <nav id="nav">
        <router-link to="/">Home</router-link>
        <span style="margin-right: 20px" ></span>
        <router-link to="/about">About</router-link>
      </nav>
      </nav>
    </div>
    <div>
      <div>
        <img class="slack-logo" src="../assets/slack-icon.png" alt="slack-logo">
        <div class="heading">
          <h1 class="main-title">Learn programming</h1>
          <h2 class="main-subtitle">A slack channel dedicated to helping others learn to program. Chat with peers and mentors to learn more about programming, and have a good time. All are welcome regardless of skill level, programming language, or age! Learn, discuss and connect. Join now.</h2>
        </div>
        <p class="main-paragraph" >Already have an account? <a target="_blank" href="https://learn-programming.slack.com/">Sign in here</a></p>
          <a target="_blank" href="https://learn-programming.slack.com/"><button id="cta-btn">Join <span class="bold">150+</span> members now</button></a>
      </div>
      <!-- <div class="right-col">
        <img id="chat-window" src="../assets/chat_window.png" alt="slack chat window" />
        <p id="powered-by-slack">Powered by Slack</p>
      </div> -->
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
$purple: #251d35;
$white: #fff;
$btn-green: #66bb42;

$breakpoints: (
  phone: 320px,
  tablet: 768px,
  desktop: 1024px
);

.slack-logo {
  width: 130px;
}

.wrapper {
  width: 100%;
  min-height: 100vh;
  height: 100%;
  background-color: $purple;

  @media (min-width: 900px) {
    height: 100vh;
  }
}

.nav {
  display: flex;
}

.main-title {
  text-align: center !important;
  font-weight: bolder;
  color: $white;
  text-transform: uppercase;
  letter-spacing: 2px;
  font-size: 4em !important;
  width: 100%;
  display: block;

  @include media('>=phone', '<=tablet') {
    font-size: 3rem;
    padding: {
      left: 4rem;
      right: 4rem;
    }
  }
}

.main-subtitle {
  font-weight: normal;
  width: 50%;
  line-height: 28px;
  color: $white;
  font-size: 1.75em;
  padding-top: 10px;
  padding-bottom: 20px;
  opacity: 0.7;

  @include media('>=phone', '<=tablet') {
    width: 90%;
  }
}

.main-paragraph {
  font-size: 1.5em;
  color: $white;

  a {
    text-decoration: underline;
    color: $white;
  }
}

.heading {
  margin-top: 3rem;
  display: flex;
  flex-direction: column;
  align-items: center;
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

  @include media('>=desktop') {
    width: 90%;
  }
}

#cta-btn {
  cursor: pointer;
  background-color: $btn-green;
  outline: none;
  border: 0;
  color: $white;
  padding: 20px 30px 20px 30px;
  font-size: 1.75em;
  border-radius: 50px;
  margin: 0 auto;
  margin-top: 2rem;
  margin-bottom: 2rem;
  transition: 0.2s ease-out 0s;

  &:hover {
    background-color: darken($btn-green, 10%);
    transition: 0.2s ease-out 0s;
  }
}

.bold {
  font-weight: 700;
}

#nav {
  padding: 2rem;
  font-weight: bold;

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
