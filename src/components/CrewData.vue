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

<style scoped>
.subtitle {
  font-family: "Bellefair";
  font-weight: 100;
  font-size: 32px;
  text-transform: uppercase;
  color: #ffffff;
  opacity: 0.5;
  margin: 120px 0 30px 0;
  letter-spacing: 1px;
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
  margin-top: 50px;
  width: 59%;
  min-height: 200px;
}
</style>
