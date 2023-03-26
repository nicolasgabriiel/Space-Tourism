<template>
  <section></section>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { subtitle, title, description } from "../assets/ts/CrewData";
export default defineComponent({
  name: "Crew-Data",
  data() {
    return {
      subtitle: subtitle as [],
      title: title as [],
      description: description as [],
    };
  },
});
</script>

<style scoped></style>
