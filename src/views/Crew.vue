<template>
    <section class="background">
        <HeaderHome/>
        <h1><span>01</span> pick your crew</h1>

    </section>
  
</template>
<script lang="ts">
import { defineComponent } from 'vue';
import HeaderHome from '@/components/HeaderHome.vue';


export default defineComponent({
    name: 'Destination-Page',
    components:{
        HeaderHome,
    }
})
</script>

<style scoped>
.background{
  width: 100%;
  height: 100vh;
  background-image: url(../assets/crew/background-crew-desktop.jpg);
  background-size: cover;
}
</style>
