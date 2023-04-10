<template>
  <header>
    <div>
      <router-link to="/"
        ><div><img src="../assets/img/shared/logo.svg" alt="" class="logo" /></div
      ></router-link>
      <div class="linha"></div>
    </div>
    <nav class="nav-header">
      <router-link to="/">
        <button class="botoes-header" :class="{ active: Home }">
          <p class="descricao-header"><strong>00</strong>Home</p>
        </button>
      </router-link>
      <router-link to="/destination">
        <button class="botoes-header" :class="{ active: Destination }">
          <p class="descricao-header"><strong>01</strong>Destination</p>
        </button>
      </router-link>
      <router-link to="/crew">
        <button class="botoes-header" :class="{ active: Crew }">
          <p class="descricao-header"><strong>02</strong>Crew</p>
        </button>
      </router-link>
      <router-link to="/technology">
        <button class="botoes-header" :class="{ active: Technology }">
          <p class="descricao-header"><strong>03</strong>Technology</p>
        </button>
      </router-link>
    </nav>
  </header>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "HeaderHome",
  data() {
    return {};
  },
  props: {
    Home: {
      type: Boolean,
      default: false,
    },
    Destination: {
      type: Boolean,
      default: false,
    },
    Crew: {
      type: Boolean,
      default: false,
    },
    Technology: {
      type: Boolean,
      default: false,
    },
  },
});
</script>

<style scoped>
header {
  display: flex;
  width: 95%;
  margin-left: 5%;
  height: 96px;
  padding-top: 40px;
  align-items: center;
  justify-content: space-between;
}
.logo {
}
.linha {
  max-width: 1000px;
  width: 200%;
  height: 1px;
  background: white;
  opacity: 0.25;
  margin-left: 250px;
  z-index: 999;
  display: absolute;
  top: -100px;
}
.nav-header {
  width: 70%;
  background: rgba(255, 255, 255, 0.04);
  backdrop-filter: blur(40.7742px);
  height: 100%;
  display: flex;
  align-items: center;
}
.botoes-header:first-child {
  margin-left: 35%;
}
.botoes-header {
  background: none;
  border: none;
  margin-right: 70px;
  padding-bottom: 33px;
  cursor: pointer;
}
.botoes-header:hover {
  border-bottom: 4px solid #cccccc;
}
strong {
  font-weight: bold;
  margin-right: 15%;
}
.descricao-header {
  margin-top: 35px;
  color: white;
  font-size: 19px;
  text-transform: uppercase;
  letter-spacing: 3px;
  font-family: "Barlow Condensed", sans-serif;
}
.active {
  border-bottom: 4px solid white;
}

/* RESPONSIVO */

@media screen and (max-width: 800px) {
}
</style>
