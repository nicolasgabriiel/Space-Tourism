<template>
    <header>
        <div><img src="../assets/shared/logo.svg" alt=""></div>
        <div class="linha"></div>
        <nav class="nav-header">
            <router-link to="/">
                <button class="botoes-header" :class="{active: Home}" @click="mudartela('home')">
                <p class="descricao-header">
                    <strong>01</strong>Home
                </p>
            </button>
            </router-link>
            <router-link to="/destination">
                <button class="botoes-header" :class="{active: Destination}" @click="mudartela('destination')" >
                    <p class="descricao-header" >
                        <strong>02</strong>Destination
                    </p>
                </button>
            </router-link>
            <button class="botoes-header" :class="{active: Crew} " @click="mudartela('crew')">
                <p class="descricao-header" >
                    <strong>03</strong>Crew
                </p>
            </button>
            <button class="botoes-header" :class="{active: Technology}" @click="mudartela('technology')">
                <p class="descricao-header" >
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
    data(){
        return{
            Home: false,
            Destination: false,
            Crew: true,
            Technology: false
        }
    },
    methods:{
        mudartela(evento:string){
          if(evento === "home"){
            
            this.Destination = false;
            this.Crew = false;
            this.Technology = false;
            this.Home = true;

          }else if(evento === "destination"){
            
            this.Crew = false;
            this.Technology = false;
            this.Home = false;
            this.Destination = true;

          }else if(evento === 'crew'){
           
            this.Technology = false;
            this.Home = false;
            this.Destination = false;
            this.Crew = true;

          }else{
            
            this.Home = false;
            this.Destination = false;
            this.Crew = false;
            this.Technology = true;

          }
        },
    
    },


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
    margin-right: 70px;
    padding-bottom: 68px;
    cursor: pointer;

}
.botoes-header:hover{
    border-bottom: 4px solid #cccccc;
}
strong{
    font-weight: bold;
    margin-right: 20px;
}
.descricao-header{
    color: white;
    font-size: 19px;
    text-transform: uppercase;
    letter-spacing: 3px;
    font-family:'Barlow Condensed', sans-serif;
}
.active{
    border-bottom: 4px solid white;
    
}
</style>
