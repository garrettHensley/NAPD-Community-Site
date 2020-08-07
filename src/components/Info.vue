<template>
  <b-container class="mt-2 text-light lead">
    <b-row class="bg-main mb-2">
      <b-col class="align-items-center">
        <h1 class="display-3 text-center my-auto">About</h1>
      </b-col>
    </b-row>
    <b-row class="mb-2">
      <b-col id="about" class="bg-main">
        <div class="p-2">
          <p>
            NAPD began as a collaboration between two friends in an effort to
            revive the Chivalry: Medieval Warfare community. NA Public Duelyard
            (NAPD) became one of the most played Chivalry servers in North
            America. As time went on, NAPD grew from a small group of friends to
            a community of nearly one thousand.
          </p>
          <p>
            Today, NAPD continues to grow and reach out into other games. In
            Mordhau, NAPD ranks in the top 25 most played servers in the world.
            Although NAPD continues to reach out to more players, we remain
            grounded in our common goals. NAPD will always be about the
            community, not the name recognition.
          </p>
        </div>
      </b-col>
    </b-row>
    <b-row id="rules" class="bg-main mb-2">
      <b-col class="align-items-center">
        <h1 class="display-3 text-center my-auto">Rules</h1>
      </b-col>
    </b-row>
    <b-row>
      <b-col class="bg-main">
        <div id="FFA" class="p-2">
          <h2 class="text-center">FFA</h2>
          <ol>
            <li>No vote kicking.</li>
            <li>No extreme toxicity (i.e. racism, homophobia, etc)</li>
            <li>
              The television (located at the church) should not display content
              including, but not limited to; nudity, pornography, racism,
              homophobia, xenophobia, transphobia, bigotry, pirated content, or
              any other form of content deemed overly toxic or inappropriate.
            </li>
          </ol>
        </div>
      </b-col>
      <b-col id="knightbg" class="d-none d-sm-block"></b-col>
    </b-row>
    <b-row class="my-2">
      <b-col id="duelbg" class="d-none d-sm-block"></b-col>
      <b-col class="bg-main">
        <div id="duels" class="p-2">
          <h2 class="text-center">Duels</h2>
          <ol>
            <li>Both players must bow or flourish to duel.</li>
            <li>Do not harass a player if he/she refuses to duel.</li>
            <li>RDM-ing will not be tolerated.</li>
            <li>Do not RDM in retaliation. Tell an admin or votekick.</li>
            <li>Accidental hits should not be an excuse of random.</li>
            <li>Do not disrespect admins.</li>
            <li>Do not harass admins.</li>
            <li>No constant ping above 140.</li>
            <li>No fire/smoke bombs.</li>
            <li>Throwable melee weapons are allowed.</li>
            <li>Do not use alternative/smurf accounts.</li>
            <li>Do not build in the duel server.</li>
            <li>Do not lay down bear traps.</li>
            <li>Do not votekick unless there is no admin online.</li>
          </ol>
          <p class="small text-muted">
            <em
              >*Any violation of these rules will be met with swift action by
              NAPD admins.</em
            >
          </p>
          <p class="small text-muted">
            <em
              >*If you see a player violating the rules, we encourage that you
              report the player to the NAPD discord in the #player-reports
              channel.</em
            >
          </p>
        </div>
      </b-col>
    </b-row>
    <b-row>
      <b-col class="bg-main">
        <div id="admins" class="p-2">
          <h2 class="text-center">Admins</h2>
          <p class="text-muted small">
            <em
              >NAPD admins are responsible with enforcing the rules as well as
              promoting stability within in the FFA server. All admins can carry
              the 1411 (the gun), but are obligated to respect the follow
              protocol</em
            >
          </p>
          <ol>
            <li>Admins may use the 1411 for self-defense.</li>
            <li>Admins may shoot if they are actively avoiding combat.</li>
            <li>Admins may shoot if they are repeatedly targeted.</li>
            <li>Admins cannot use the 1411 to help secure the catapult.</li>
            <li>
              Admins cannot use the 1411 to intentionally attack others (unless
              attacked first).
            </li>
            <li>
              Admins cannot use the 1411 in mid combat after attacking first
              with a melee weapon.
            </li>
            <li>
              Admins who are overseeing a specific duel within the fort may
              shoot players who wish to interrupt the duel.
            </li>
            <li>
              If an admin shoots, misses, and hits another player by accident,
              it does not count as admin abuse, but are encouraged to
              apologized.
            </li>
            <li>
              Admins may use the 1411 to shoot the rocks or shoot at the
              catapult if being fired at them.
            </li>
            <li>
              If an admin asks you to stop being toxic or end a conversation and
              you do not respect their warning, they ultimately deserve the
              right to mute or ban you at their discretion.
            </li>
          </ol>
        </div>
      </b-col>
      <b-col id="adminbg" class="d-none d-sm-block"></b-col>
    </b-row>
    <b-row class="bg-main mt-2 mb-2">
      <b-col class="align-items-center">
        <h1 class="display-3 text-center my-auto">Servers</h1>
      </b-col>
    </b-row>
    <b-row>
      <b-col class="servers">
        <Servers @playerCount="playerCount" />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import Servers from "@/components/Servers.vue";
export default {
  components: {
    Servers
  },
  methods: {
    playerCount: function(e) {
      this.$emit("playerCount", e);
    }
  }
};
</script>

<style>
.col {
  -webkit-box-shadow: 10px 10px 5px -7px rgba(0, 0, 0, 0.35);
  -moz-box-shadow: 10px 10px 5px -7px rgba(0, 0, 0, 0.35);
  box-shadow: 10px 10px 5px -7px rgba(0, 0, 0, 0.35);
}
.active {
  background: linear-gradient(45deg, #ff7272, #ffb3b3) !important;
}
a {
  color: white;
}
#FFA {
}
.servers {
  box-shadow: none !important;
  padding: 0 !important;
}
ol li {
  margin-bottom: 0.6em;
}
#knightbg {
  background-image: url(~@/assets/ffabg.png);
  background-size: 40em;
}
#duelbg {
  background-image: url(~@/assets/duelbg.png);
  background-size: 80em;
  background-position-x: -30em;
}
#adminbg {
  background-image: url(~@/assets/adminbg.png);
  background-size: 85em;
  background-position-x: -19em;
}
</style>
