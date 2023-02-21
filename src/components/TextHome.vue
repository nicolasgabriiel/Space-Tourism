<template>
    <main>
        <h2>So, you want to travel to</h2>
        <h1>Space</h1>
        <h3>
        Let’s face it; if you want to go to space, you might as well genuinely go to 
        outer space and not hover kind of on the edge of it. Well sit back, and relax 
        because we’ll give you a truly out of this world experience!
        </h3>
    </main>
</template>

<style scoped>
main{
    width: 31.25%;
    font-family:'Barlow Condensed', sans-serif;
    margin: 200px 0 0 200px;
}
main h2{
    color: #D0D6F9;
    font-size: 28px;
    letter-spacing: 5px;
    text-transform: uppercase;
}
main h1{
    color: #ffffff;
    font-size: 180px;
    letter-spacing: 10px;
    margin: 25px 0 50px 0;
    text-transform: uppercase;
}
main h3{
    font-size: 20px;
    color: #D0D6F9;
    line-height:32px;
    letter-spacing: 3px;
    width: 80%;
}
</style>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name:'Text-Home',
})
</script>
