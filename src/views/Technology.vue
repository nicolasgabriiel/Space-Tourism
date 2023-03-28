<template>
  <section class="background">
    <HeaderHome :Technology="Technology" />
    <div class="title-container">
      <h1 class="title">01</h1>
      <h1 class="title2">space launch 101</h1>
    </div>
    <div class="container-data">
      <div class="left">
        <div class="button-controler">
          <button
            class="button"
            :class="{ active: ControlerData[0] }"
            @click="trocarTela(0)"
          >
            1
          </button>
          <button
            class="button"
            :class="{ active: ControlerData[1] }"
            @click="trocarTela(1)"
          >
            2
          </button>
          <button
            class="button"
            :class="{ active: ControlerData[2] }"
            @click="trocarTela(2)"
          >
            3
          </button>
        </div>
      </div>
      <div class="center">
        <TechnologyData :Indice="Indice" />
      </div>
      <div class="rigth">
        <TechnologyImage :ControlerData="ControlerData" />
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import HeaderHome from "@/components/HeaderHome.vue";
import TechnologyData from "@/components/TechnologyData.vue";
import TechnologyImage from "@/components/TechnologyImage.vue";
import { defineComponent } from "vue";
export default defineComponent({
  name: "Technology-Page",
  components: { HeaderHome, TechnologyData, TechnologyImage },
  data() {
    return {
      Technology: true,
      ControlerData: [true, false, false],
      Indice: 0,
    };
  },
  methods: {
    trocarTela(indice: number) {
      this.ControlerData = [false, false, false];
      if (indice == 0) {
        this.ControlerData[0] = true;
        this.Indice = 0;
      } else if (indice == 1) {
        this.ControlerData[1] = true;
        this.Indice = 1;
      } else {
        this.ControlerData[2] = true;
        this.Indice = 2;
      }
    },
  },
});
</script>

<style scoped>
.background {
  width: 100%;
  height: 100vh;
  background-image: url(../assets/img/technology/background-technology-desktop.jpg);
  background-size: cover;
}
.title-container {
  display: flex;
  flex-direction: row;
  margin: 100px 0 0 250px;
  font-family: "Barlow Condensed", sans-serif;
}
.title {
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
.container-data {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.left {
  width: 20%;
}
.center {
  width: 40%;
}
.right {
  width: 40%;
}
.button-controler {
  display: flex;
  flex-direction: column;
  margin-left: 250px;
}
.button {
  width: 80px;
  height: 80px;
  border: 1px solid rgba(255, 255, 255, 0.25);
  background: transparent;
  border-radius: 40px;
  font-family: "Bellefair", serif;
  font-size: 32px;
  color: white;
  text-align: center;
  margin: 20px 0;
  cursor: pointer;
  transition: 0.3s;
}
.button:hover {
  border: 1px solid rgb(255, 255, 255) !important;
}
.active {
  border: 1px solid rgb(255, 255, 255) !important;
  background: white !important;
  color: black !important;
}
</style>
