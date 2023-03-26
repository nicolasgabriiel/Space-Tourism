<template>
  <section>
    <h2 class="subtitle">{{ subtitle[indice] }}</h2>
    <h1 class="title">{{ title[indice] }}</h1>
    <p class="description">{{ description[indice] }}</p>
  </section>
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
  props: {
    indice: {
      type: Number,
      default: 0,
    },
  },
});
</script>

<style scoped></style>
