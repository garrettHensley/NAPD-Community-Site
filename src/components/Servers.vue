<template>
  <b-card-group deck>
    <b-card
      v-for="server in info"
      :key="server.id"
      :header="server.attributes.name"
      :footer="server.attributes.status"
      class="bg-main text-center rounded-0 border-0"
      :class="{ 'text-muted': server.attributes.status != 'online' }"
      :header-bg-variant="
        server.attributes.status === 'online' ? 'success' : 'danger'
      "
    >
      <b-card-text class="text-left">
        <b-avatar></b-avatar> {{ server.attributes.players }} /
        {{ server.attributes.maxPlayers }}
      </b-card-text></b-card
    >
  </b-card-group>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      info: [],
      servers: ["7814064", "7839657", "7057086"]
    };
  },
  mounted() {
    for (let i = 0; i < this.servers.length; i++) {
      console.log("test");
      axios
        .get(`https://api.battlemetrics.com/servers/${this.servers[i]}`)
        .then(response => this.info.push(response.data.data)); // data.data lol 🤔
    }
    setTimeout(this.getPlayerCount, 370);
  },
  methods: {
    getPlayerCount: function() {
      let add = 0;
      for (let i = 0; i < this.servers.length; i++) {
        add += this.info[i].attributes.players;
      }

      this.$emit("playerCount", add);
    }
  }
};
</script>

<style>
.card {
  -webkit-box-shadow: 10px 10px 5px -7px rgba(0, 0, 0, 0.35);
  -moz-box-shadow: 10px 10px 5px -7px rgba(0, 0, 0, 0.35);
  box-shadow: 10px 10px 5px -7px rgba(0, 0, 0, 0.35);
}
.card-header,
.card-footer {
  border-radius: 0 !important;
  text-transform: capitalize;
}
</style>
