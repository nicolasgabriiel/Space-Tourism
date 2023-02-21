<template>
  <section class="background">
    <h1>HOME</h1> 
  </section>
  
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HomeView',
});
</script>

<style scoped>
.background{
  width: 100%;
  height: 100vh;
  background-image: url(../assets/home/background-home-desktop.jpg);
  background-size: cover;
}
</style>

