<template>
  <main>
    <h2>So, you want to travel to</h2>
    <h1>Space</h1>
    <h3>
      Let’s face it; if you want to go to space, you might as well genuinely go to outer
      space and not hover kind of on the edge of it. Well sit back, and relax because
      we’ll give you a truly out of this world experience!
    </h3>
  </main>
</template>

<style scoped>
main {
  width: 31.25%;
  font-family: "Barlow Condensed", sans-serif;
  margin: 200px 0 0 200px;
}
main h2 {
  color: #d0d6f9;
}
main h1 {
}
main h3 {
  width: 82%;
}
@media screen and (max-width: 800px) {
}
</style>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Text-Home",
});
</script>
