<template>
  <section class="background">
    <HeaderHome :Crew="Crew" />
    <div class="title-container">
      <h1 class="title1">02</h1>
      <h1 class="title2">meet your crew</h1>
    </div>
    <div class="container">
      <div class="left">
        <CrewData :indice="indice" />
        <div class="controler-crew">
          <button
            class="button"
            :class="{ active: controler[0] }"
            @click="trocarTema(0)"
          ></button>
          <button
            class="button"
            :class="{ active: controler[1] }"
            @click="trocarTema(1)"
          ></button>
          <button
            class="button"
            :class="{ active: controler[2] }"
            @click="trocarTema(2)"
          ></button>
          <button
            class="button"
            :class="{ active: controler[3] }"
            @click="trocarTema(3)"
          ></button>
        </div>
      </div>
      <div class="rigth">
        <CrewImage />
      </div>
    </div>
  </section>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import HeaderHome from "@/components/HeaderHome.vue";
import CrewData from "@/components/CrewData.vue";
import CrewImage from "@/components/CrewImage.vue";

export default defineComponent({
  name: "Destination-Page",
  components: {
    HeaderHome,
    CrewData,
    CrewImage,
  },
  data() {
    return {
      Crew: true,
      controler: [true, false, false, false],
      indice: 0,
    };
  },
  methods: {
    trocarTema(number: number) {
      this.controler = [false, false, false, false];
      if (number == 0) {
        this.controler[0] = true;
        this.indice = 0;
      } else if (number == 1) {
        this.controler[1] = true;
        this.indice = 1;
      } else if (number == 2) {
        this.controler[2] = true;
        this.indice = 2;
      } else {
        this.controler[3] = true;
        this.indice = 3;
      }
    },
  },
});
</script>

<style scoped>
.background {
  width: 100%;
  height: 100vh;
  background-image: url(../assets/img/crew/background-crew-desktop.jpg);
  background-size: cover;
}

.title-container {
  display: flex;
  flex-direction: row;
  margin: 100px 0 0 250px;
  font-family: "Barlow Condensed", sans-serif;
}

.title1 {
  font-size: 30px;
  color: rgba(255, 255, 255, 0.25);
  font-weight: bold;
  text-transform: uppercase;
  letter-spacing: 5px;
  margin-right: 20px;
}

.title2 {
  font-size: 30px;
  color: white;
  font-weight: 300;
  text-transform: uppercase;
  letter-spacing: 5px;
}
.container {
  display: flex;
}
.left {
  width: 50%;
  margin-left: 250px;
}
.right {
  width: 50%;
}
.controler-crew {
  display: flex;
  margin: 0 0 0 10px;
}

.controler-crew .button {
  width: 15px;
  height: 15px;
  background: #ffffff;
  opacity: 0.17;
  border: 0;
  border-radius: 7.5px;
  margin: 60px 15px 0 0;
}

.controler-crew .button:hover {
  cursor: pointer;
  background: #ffffff;
  opacity: 0.5;
}

.active {
  background: #ffffff !important;
  opacity: 1 !important;
}
</style>
