<template>
  <div>
    <b-container id="app" fluid>
      <Nav />
      <link rel="icon" href="../icon.ico" />
      <Logo :players="count" />
      <Info @playerCount="playerCount" />
      <p class="text-center mt-3">
        Site developed & designed by Garrett Hensley |
        <a href="http://twitter.com/garretthensleyx" target="_blank">Twitter</a>
        |
        <a href="http://github.com/garrettHensley" target="_blank">GitHub</a>
      </p>
    </b-container>
  </div>
</template>

<script>
import Logo from "@/components/Logo.vue";
import Info from "@/components/Info.vue";
import Nav from "@/components/Nav.vue";

export default {
  name: "App",
  components: {
    Logo,
    Info,
    Nav,
  },
  data() {
    return {
      img: {
        knight: require("@/assets/knight.png"),
      },
      count: null,
    };
  },
  methods: {
    playerCount(e) {
      this.count = e;
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat&display=swap");

#app {
}
html body {
  background-image: url("~@/assets/bg.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
  font-family: "Montserrat", sans-serif;
}
@media only screen and (min-device-width: 320px) and (max-device-width: 480px) and (-webkit-min-device-pixel-ratio: 2) and (orientation: portrait) {
  html body {
    /* The file size of this background image is 93% smaller
       to improve page load speed on mobile internet connections */
    background: linear-gradient(
      45deg,
      rgba(255, 52, 56, 1) rgba(120, 5, 251, 1)
    );
    background-size: cover;
  }
}
h1 {
  font-family: "Pinyon Script", cursive;
}
.bg-main {
  background-color: #2b2928da !important;
  color: rgb(235, 235, 255);
}
.lead {
  font-weight: 100;
}
</style>
