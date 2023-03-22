<template>
    <section class="background">
        <header>
            <HeaderHome :Destination="Destination"/>
        </header>
        <main class="principal">
            <div class="title-container">
                <h1 class="title">01</h1>
                <h1 class="title2"> pick your destination</h1>
            </div>
            
            <div>
                <DestinationControler class="hide"/>
            </div>
        </main>
    </section>
  
</template>
<script lang="ts">
import { defineComponent } from 'vue';
import HeaderHome from '@/components/HeaderHome.vue';
import DestinationControler from '@/components/DestinationControler.vue';

export default defineComponent({
    name: 'Destination-Page',
    components:{
        HeaderHome,
        DestinationControler
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
.hide{
    display: none;
}
.principal{
    font-family:'Barlow Condensed', sans-serif;
}
.title-container{
    display: flex;
    flex-direction: row;
    margin: 100px 0 0 250px;
}
.title{
    font-size: 30px;
    color: rgba(255, 255, 255, 0.25);
    font-weight:bold;
    text-transform: uppercase;
    letter-spacing: 5px;
    margin-right: 20px;
}
.title2{
    font-size: 30px;
    color: white;
    font-weight: 300;
    text-transform: uppercase;
    letter-spacing: 5px;
}


</style>
