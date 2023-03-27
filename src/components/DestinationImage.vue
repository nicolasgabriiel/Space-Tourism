<template>
  <div>
    <img src="../assets/img/destination/image-moon.png" :class="{ hide: !moon }" />
    <img src="../assets/img/destination/image-mars.png" :class="{ hide: !mars }" />
    <img src="../assets/img/destination/image-europa.png" :class="{ hide: !europa }" />
    <img src="../assets/img/destination/image-titan.png" :class="{ hide: !titan }" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Destination-Image",

  props: {
    moon: {
      type: Boolean,
      default: false,
    },
    mars: {
      type: Boolean,
      default: false,
    },
    europa: {
      type: Boolean,
      default: false,
    },
    titan: {
      type: Boolean,
      default: false,
    },
  },
});
</script>

<style scoped>
.hide {
  display: none !important;
}
img {
  margin: 100px 0 0 220px;
}
</style>
