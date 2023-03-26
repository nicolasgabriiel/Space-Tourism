<template>
  <section class="background">
    <HeaderHome :Crew="Crew" />
    <div class="title-container">
      <h1 class="title1">02</h1>
      <h1 class="title2">pick your crew</h1>
    </div>
    <div class="container">
      <div class="left">
        <!--CrewData-->
        <div class="controler-crew"></div>
      </div>
      <div class="rigth">
        <!--CrewImage-->
      </div>
    </div>
  </section>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import HeaderHome from "@/components/HeaderHome.vue";

export default defineComponent({
  name: "Destination-Page",
  components: {
    HeaderHome,
  },
  data() {
    return {
      Crew: true,
    };
  },
});
</script>

<style scoped>
.background {
  width: 100%;
  height: 100vh;
  background-image: url(../assets/crew/background-crew-desktop.jpg);
  background-size: cover;
}
</style>
