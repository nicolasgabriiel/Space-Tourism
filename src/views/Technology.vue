<template>
  <section>
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

<style scoped></style>
