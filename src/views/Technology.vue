<template>
  <section class="background">
    <HeaderHome :Technology="Technology" />
    <div class="title-container">
      <h1 class="title">01</h1>
      <h1 class="title2">space launch 101</h1>
    </div>
    <div class="container-data">
      <div class="left"></div>
      <div class="center"></div>
      <div class="rigth"></div>
    </div>
  </section>
</template>

<script lang="ts">
import HeaderHome from "@/components/HeaderHome.vue";
import { defineComponent } from "vue";
export default defineComponent({
  name: "Technology-Page",
  components: { HeaderHome },
  data() {
    return {
      Technology: true,
    };
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
</style>
