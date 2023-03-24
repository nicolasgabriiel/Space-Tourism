<template>
  <div>
    <img src="../assets/destination/image-moon.png" :class="{ hide: !moon }" />
    <img src="../assets/destination/image-mars.png" :class="{ hide: !mars }" />
    <img src="../assets/destination/image-europa.png" :class="{ hide: !europa }" />
    <img src="../assets/destination/image-titan.png" :class="{ hide: !titan }" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

// import { linkImage } from "@/assets/DestinationData";
// link: linkImage as string[],

export default defineComponent({
  name: "Destination-Image",
  data() {
    return {};
  },
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
