<template>
  <div>
    <img :src="linkImages[0]" />
    <img src="../assets/destination/image-europa.png" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

import { linkImage } from "@/assets/DestinationData";

export default defineComponent({
  name: "Destination-Image",
  data() {
    return {
      linkImages: linkImage as string[],
    };
  },
  mounted() {
    console.log(this.linkImages[2]);
  },
});
</script>

<style scoped></style>
