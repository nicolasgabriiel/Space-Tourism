<template>
  <div>
    <img :src="link[3]" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

import { linkImage } from "@/assets/DestinationData";

export default defineComponent({
  name: "Destination-Image",
  data() {
    return {
      link: linkImage as string[],
    };
  },
});
</script>

<style scoped></style>
