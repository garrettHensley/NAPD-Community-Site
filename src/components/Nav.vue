<template>
  <div>
    <b-navbar fixed="top" toggleable="lg">
      <b-navbar-brand href="#">
        <b-img :src="img.logo" style="width: 3em;" />
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#about">About</b-nav-item>
          <b-nav-item-dropdown text="Rules" right>
            <b-dropdown-item href="#rules">Overview</b-dropdown-item>
            <b-dropdown-item href="#FFA">FFA</b-dropdown-item>
            <b-dropdown-item href="#duels">Duels</b-dropdown-item>
            <b-dropdown-item href="#admins">Admin</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      img: {
        logo: require("@/assets/logo.png")
      }
    };
  }
};
</script>

<style scoped>
.navbar {
  backdrop-filter: blur(0.1em);
}
</style>
