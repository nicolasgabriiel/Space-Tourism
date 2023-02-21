<template>
    <header>
        <div><img src="../assets/shared/logo.svg" alt=""></div>
        <div class="linha"></div>
        <nav class="nav-header">
        
            <button class="botoes-header">
                <p class="descricao-header">
                    <strong>01</strong>Home
                </p>
            </button>
            <button class="botoes-header">
                <p class="descricao-header">
                    <strong>02</strong>Destination
                </p>
            </button>
            <button class="botoes-header">
                <p class="descricao-header">
                    <strong>03</strong>Crew
                </p>
            </button>
            <button class="botoes-header">
                <p class="descricao-header">
                    <strong>03</strong>Technology
                </p>
            </button>
        </nav>
    </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: 'HeaderHome',

})
</script>

<style scoped>
header {
    display: flex;
    width: 95%;
    margin-left: 5%;
    height: 96px;
    padding-top: 40px;
    align-items: center;
    justify-content: space-between;
    font-family:'Barlow Condensed', sans-serif;



}

.linha {
    width: 473px;
    height: 1px;
    background: white;
    opacity: 0.25;
    display: absolute;
    margin-left: 300px;
    z-index: 999;

}
.nav-header {
    width: 65%;
    background: rgba(255, 255, 255, 0.04);
    backdrop-filter: blur(40.7742px);
    height: 100%;
    display: flex;
    align-items: center;
}
.botoes-header:first-child{
    margin-left:100px;
}
.botoes-header{
    background: none;
    border: none;
    
}
strong{
    font-weight: bold;
    margin-right: 20px;
}
.descricao-header{
    color: white;
    font-size: 19px;
    margin-right: 70px;
    text-transform: uppercase;
    letter-spacing: 3px;
    font-family:'Barlow Condensed', sans-serif;
    
}
</style>
