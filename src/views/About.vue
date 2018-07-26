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
          <h1 class="main-title">About</h1>
          <p class="about-paragraph">A slack channel dedicated to helping others learn to program. Chat with peers and mentors to learn more about programming, and have a good time. All are welcome regardless of skill level, programming language, or age!
          We currently have members from over 10 different countries from around the world, so you'll be getting diverse opinions on matters. The goal is to help you learn, and learn right.</p>
        </div>

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
  name: "about",
  components: {}
};
</script>

<style lang="scss">
@import "../assets/_include-media.scss";
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

  @include media(">=phone", "<=tablet") {
    font-size: 3rem;
  }
}

.about-paragraph {
  font-weight: normal;
  width: 50%;
  line-height: 28px;
  color: $white;
  font-size: 1.75em;
  padding-top: 10px;
  padding-bottom: 20px;
  opacity: 0.7;

  @include media(">=phone", "<=tablet") {
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

  @include media(">=desktop") {
    width: 90%;
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
