<template>
  <section class="background">
    <HeaderHome :Home="Home"/>
    <div class="container">
      <TextHome />
      <div class="centralizar">
        <div class="fundo_botao" v-bind:class="{'ampliado': expandir}">
          <router-link to="/destination">
            <button class="explore" v-on:mouseover="expandir = true" v-on:mouseout="expandir = false">Explore</button>
          </router-link>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HeaderHome from '@/components/HeaderHome.vue';
import TextHome from '@/components/TextHome.vue';

export default defineComponent({
  name: 'HomeView',
  components: {
    HeaderHome,
    TextHome
  },
  data() {
    return {
      fundo: false,
      expandir: false,
      Home: true
    }
  },
  methods:{
    onHover(){
      this.expandir = true
    }
  }

});
</script>

<style scoped>
.background {
  width: 100%;
  height: 100vh;
  background-image: url(../assets/home/background-home-desktop.jpg);
  background-size: cover;
}

.container {
  display: flex;
  justify-content: space-between;
}
.centralizar{
  display: flex;
  justify-content: center;
}
.explore {
  width: 274px;
  height: 274px;
  border-radius: 137px;
  border: none;
  background-color: white;
  font-size: 37px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: black;
  font-family: 'Barlow Condensed', sans-serif;
  position: relative;

}
.fundo_botao {
  position: relative;
  border-radius: 225px;
  background-color: rgba(255, 255, 255, 0.2);
  margin: 250px  200px 0 0;
  transition: .5 s;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: width 1s ease, height 1s ease, margin 1s ease;
  width: 274px;
  height: 274px;
}
.fundo_botao.ampliado {
  width: 450px;
  height: 450px;
  margin: 162px  112px 0 0;
}

.fundo_botao:hover .explore {
  cursor: pointer;
}
</style>

