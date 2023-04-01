<template>
  <div>
    <div class="container-imagem imagem1" :class="{ hide: !controler[0] }"></div>
    <div class="container-imagem imagem2" :class="{ hide: !controler[1] }"></div>
    <div class="container-imagem imagem3" :class="{ hide: !controler[2] }"></div>
    <div class="container-imagem imagem4" :class="{ hide: !controler[3] }"></div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  name: "Crew-Image",
  props: {
    controler: {
      default: [true, false, false, false],
    },
  },
});
</script>

<style scoped>
.container-imagem {
  width: 700px;
  height: 673px;
  background-position: bottom;
  background-size: contain;
  background-repeat: no-repeat;
}
.hide {
  display: none !important;
}
.imagem1 {
  background-image: url("../assets/img/crew/image-douglas-hurley.png");
}
.imagem2 {
  background-image: url("../assets/img/crew/image-mark-shuttleworth.png");
}
.imagem3 {
  background-image: url("../assets/img/crew/image-victor-glover.png");
}
.imagem4 {
  background-image: url("../assets/img/crew/image-anousheh-ansari.png");
}
/* alterarbg */
</style>
