<template>
  <section>
    <h2>The terminology...</h2>
    <h1>{{ TechTitle[Indice] }}</h1>
    <p>{{ TechDescription[Indice] }}</p>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { title, description } from "../assets/ts/TechnologyData";
export default defineComponent({
  name: "Technology-Data",
  data() {
    return {
      TechTitle: title as [],
      TechDescription: description as [],
    };
  },
  props: {
    Indice: {
      default: 0,
    },
  },
});
</script>

<style></style>
