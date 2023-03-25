<template>
  <div>
    <h1 class="title">{{ title[indice] }}</h1>
    <p class="description">{{ description[indice] }}</p>
    <div class="linha"></div>
    <div class="container">
      <div class="left">
        <h3>avg. distance</h3>
        <h2>{{ kms[indice] }}</h2>
      </div>
      <div class="right">
        <h3>est. travel time</h3>
        <h2>{{ years[indice] }}</h2>
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
    indice: {
      type: Number,
      default: 0,
    },
  },
});
</script>

<style scoped></style>

// if (this.moon == true) { // this.indice = 0; // console.log(this.indice); // } else if
(this.mars == true) { // this.indice = 1; // console.log(this.indice); // } else if
(this.europa == true) { // this.indice = 2; // console.log(this.indice); // } else { //
this.indice = 3; // console.log(this.indice); // }
