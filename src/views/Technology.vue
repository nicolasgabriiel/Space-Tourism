<template>
  <section class="background">
    <HeaderHome :Technology="Technology" />
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
</style>
