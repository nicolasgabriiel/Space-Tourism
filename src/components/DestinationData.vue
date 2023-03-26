<template>
  <div class="container-data">
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

<style scoped>
.container-data {
  display: flex;
  flex-direction: column;
  width: 50%;
}
.title {
  font-family: "Bellefair", serif;
  font-size: 100px;
  line-height: 115px;
  color: white;
  text-transform: uppercase;
  margin: 30px 0 20px 0;
}
.description {
  font-family: "Barlow Condensed", sans-serif;
  font-size: 22px;
  font-weight: 200;
  line-height: 32px;
  color: #d0d6f9;
  letter-spacing: 1px;
}
.linha {
  width: 100%;
  height: 1px;
  background-color: #383b4b;
  margin: 55px 0 30px 0;
}
.container {
  display: flex;
  justify-content: space-between;
}
.right h3,
.left h3 {
  font-family: "Barlow Condensed", sans-serif;
  font-size: 16px;
  font-weight: 200;
  line-height: 32px;
  color: #d0d6f9;
  text-transform: uppercase;
  letter-spacing: 1px;
}
.right h2,
.left h2 {
  font-family: "Bellefair", serif;
  font-style: normal;
  font-weight: 400;
  font-size: 28px;
  line-height: 32px;
  text-transform: uppercase;
  color: #ffffff;
}
</style>

<script lang="ts">
import { defineComponent } from "vue";
import { title, description, kms, years } from "../assets/ts/DestinationData";
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
