<template>
  <section class="background">
    <HeaderHome  />
    <div class="container">
      <TextHome/>
      <div class="fundo_botao" >
        <router-link to="/destination">
          <button class="explore" >Explore</button>
          </router-link>
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
  components:{
    HeaderHome,
    TextHome
},
data(){
  return{
    fundo: false
  }
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
.container{
  display: flex;
  justify-content: space-between;
}
.explore{
  width: 274px;
  height: 274px;
  border-radius: 137px;
  border: none;
  background-color: white;
  font-size: 37px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: black;
  font-family:'Barlow Condensed', sans-serif;
margin: 88px  0 0 88px;

}
.fundo_botao{
  width: 450px;
  height: 450px;
  border-radius: 225px;
  background-color: rgba(255, 255, 255, 0);
  margin: 200px 200px 0 0;
  transition: .5  s;
}
.fundo_botao:hover{
background-color: rgba(255, 255, 255, 0.2);
}
.fundo_botao:hover .explore{
  cursor: pointer;
}

</style>

