<template>
    <section class="background">
        <HeaderHome/>
    </section>
  
</template>
<script lang="ts">
import { defineComponent } from 'vue';
import HeaderHome from '@/components/HeaderHome.vue';

export default defineComponent({
    name: 'Destination-Page',
    components:{
        HeaderHome
    }

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
