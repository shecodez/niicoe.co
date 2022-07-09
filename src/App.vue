<template>
  <img class="avatar" alt="Niico's Avatar" src="./assets/under-construction-avatar-t.png" />
  <img class="banner" alt="Niico's Avatar" src="./assets/niico-banner.png" />
  <HelloWorld msg="Hello, World!" />
</template>

<script setup>
import HelloWorld from './components/HelloWorld.vue';

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
html,
body {
  height: 100%;
}
body {
  margin: 0;
}
a {
  color: #25e7f0;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
#app {
  background-color: #212121;
  color: #f1f1f1;
  display: flex;
  flex-direction: column;
  height: 100%;
  align-items: center;
  justify-content: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.avatar {
  height: 60%;
}
.banner {
  height: 25%;
  position: absolute;
  left: 10%;
  top: 0;
}
@media only screen and (max-width: 600px) {
  .avatar {
    height: 50%;
  }
  .banner {
    height: 15%;
  }
}
</style>
