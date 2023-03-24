<template>
  <div>
    <h1 class="title">{{ title[0] }}</h1>
    <p class="description">{{ description[0] }}</p>
    <div class="linha"></div>
    <div class="container">
      <div class="left">
        <h3>avg. distance</h3>
        <h2>{{ kms[0] }}</h2>
      </div>
      <div class="right">
        <h3>est. travel time</h3>
        <h2>{{ years[0] }}</h2>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { title, description, kms, years } from "../assets/DestinationData";
export default defineComponent({
  name: "Destination-Data",
  data() {
    return {
      title: title as string[],
      description: description as string[],
      kms: kms as string[],
      years: years as string[],
    };
  },
});
</script>

<style scoped></style>
