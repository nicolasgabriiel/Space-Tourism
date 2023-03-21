<template>
    <section class="background">
        <HeaderHome :Destination="Destination"/>
        <h1><span>01</span> pick your destination</h1>
        <DestinationComponent/>
    </section>
  
</template>
<script lang="ts">
import { defineComponent } from 'vue';
import HeaderHome from '@/components/HeaderHome.vue';
import DestinationComponent from '@/components/DestinationComponent.vue';

export default defineComponent({
    name: 'Destination-Page',
    components:{
        HeaderHome,
        DestinationComponent
    },
    data() {
    return {
        Destination: true
    }
    },
})
</script>

<style scoped>
.background{
  width: 100%;
  height: 100vh;
  background-image: url(../assets/destination/background-destination-desktop.jpg);
  background-size: cover;
}
</style>
