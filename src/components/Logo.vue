<template>
  <b-jumbotron fluid id="logo" class="text-center" header-level="1">
    <div>
      <b-img :src="img.logo" class="logo" />
      <h1>Double the Damage Double the Fun</h1>
      <div class="ml-3">
        <b-button
          href="https://discord.gg/napd"
          target="_blank"
          size="lg"
          squared
          class="mx-1 discord"
          >Discord</b-button
        >
        <b-button
          href="https://www.paypal.com/paypalme/realMantisShrimp"
          target="_blank"
          size="lg"
          squared
          class="mx-1 donate"
          >Donate</b-button
        >
        <b-button
          href="https://forms.gle/9V5xFDfWdL2eZjev5"
          target="_blank"
          size="lg"
          squared
          class="mx-1 apply"
          >Admin Application</b-button
        >
      </div>
    </div>
    <p :if="players" class="lead mt-3">{{ players }} players online</p>
  </b-jumbotron>
</template>

<script>
export default {
  data() {
    return {
      img: {
        logo: require("@/assets/logo.png")
      }
    };
  },
  props: {
    players: Number
  }
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Yeseva+One&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Pinyon+Script&display=swap");

h1 {
  font-family: "Yeseva One", cursive;
}
#logo {
  background: transparent !important;
}
#logo h1 {
  font-family: "Pinyon Script", cursive;
}
.logo {
  width: 20em;
}
.btn {
  -webkit-box-shadow: 9px 10px 0px -6px rgba(35, 39, 42, 1);
  -moz-box-shadow: 9px 10px 0px -6px rgba(35, 39, 42, 1);
  box-shadow: 9px 10px 0px -6px rgba(35, 39, 42, 0.315);
  border: 1px outset #1c6ea4;
}
.discord {
  background-color: #7289da;
}
.donate {
  background-color: #3d9cde;
}
.apply {
  background-color: #ec7063;
}
.jumbotron {
  padding-bottom: 0 !important;
}
</style>
