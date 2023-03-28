<template>
  <section class="container-image">
    <div class="imagem imagem1" :class="{ hide: !ControlerData[0] }"></div>
    <div class="imagem imagem2" :class="{ hide: !ControlerData[1] }"></div>
    <div class="imagem imagem3" :class="{ hide: !ControlerData[2] }"></div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  name: "TechnologyImage",
  props: {
    ControlerData: {
      default: [true, false, false],
    },
  },
});
</script>

<style scoped>
.imagem {
  margin-left: 202px;
  width: 586px;
  height: 600px;
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;
  background-color: red;
}
.hide {
  display: none !important;
}
.imagem1 {
  background-image: url("../assets/img/technology/image-launch-vehicle-portrait.jpg");
}
.imagem2 {
  background-image: url("../assets/img/technology/image-spaceport-portrait.jpg");
}
.imagem3 {
  background-image: url("../assets/img/technology/image-space-capsule-portrait.jpg");
}
</style>
