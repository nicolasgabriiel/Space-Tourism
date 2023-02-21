<template>
  <section class="background">
    <HeaderHome/>
  </section>
  
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HeaderHome from '@/components/HeaderHome.vue';

export default defineComponent({
  name: 'HomeView',
  components:{
    HeaderHome
  }
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

