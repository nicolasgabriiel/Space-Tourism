<template>
  <section class="container-text">
    <h2 class="subtitle">The terminology...</h2>
    <h1 class="title">{{ TechTitle[Indice] }}</h1>
    <p class="description">{{ TechDescription[Indice] }}</p>
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

<style scoped>
.subtitle {
  font-family: "Barlow Condensed", sans-serif;
  font-weight: 200;
  font-size: 16px;
  line-height: 19px;
  letter-spacing: 2.7px;
  color: #d0d6f9;
  text-transform: uppercase;
  margin: 50px 0 20px 0;
}
.title {
  font-family: "Bellefair";
  font-style: normal;
  font-weight: 400;
  font-size: 56px;
  text-transform: uppercase;
  letter-spacing: 1px;
  color: #ffffff;
}
.description {
  font-family: "Barlow Condensed", sans-serif;
  font-size: 18px;
  line-height: 32px;
  color: #d0d6f9;
  letter-spacing: 2px;
  font-weight: 200;
  margin-top: 30px;
  width: 60.7%;
  min-height: 200px;
}
.container-text {
  margin: 0 0 0 50px;
}
</style>
