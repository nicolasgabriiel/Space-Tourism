<template>
  <div class="container-data">
    <section class="esquerda">
      <DestinationImage :moon="moon" :mars="mars" :europa="europa" :titan="titan" />
    </section>
    <section class="direita">
      <div>
        <header>
          <nav class="navegacao-controle">
            <button @click="trocarEstacao('moon')">
              <h2 class="title-button" :class="{ active: moon }">moon</h2>
            </button>
            <button @click="trocarEstacao('mars')">
              <h2 class="title-button" :class="{ active: mars }">mars</h2>
            </button>
            <button @click="trocarEstacao('europa')">
              <h2 class="title-button" :class="{ active: europa }">europa</h2>
            </button>
            <button @click="trocarEstacao('titan')">
              <h2 class="title-button" :class="{ active: titan }">titan</h2>
            </button>
          </nav>
        </header>
      </div>
      <div>
        <DestinationData />
      </div>
    </section>
  </div>
</template>

<style scoped>
.container-data {
  display: flex;
}
.esquerda {
  width: 50%;
  height: 20px;
}
.direita {
  width: 50%;
}
.navegacao-controle button {
  background-color: transparent;
  border: 0;
}

.title-button {
  font-size: 16px;
  line-height: 19.2px;
  letter-spacing: 2.7px;
  color: #d0d6f9;
  text-transform: uppercase;
  margin: 50px 30px 0 0;
}
.title-button:hover {
  cursor: pointer;
  border-bottom: 4px solid #979797;
  padding-bottom: 10px;
}
.active {
  color: #ffffff;
  cursor: pointer;
  border-bottom: 4px solid white;
  padding-bottom: 10px;
  font-weight: 600;
}
</style>

<script lang="ts">
import { defineComponent } from "vue";
import DestinationImage from "./DestinationImage.vue";
import DestinationData from "./DestinationData.vue";

export default defineComponent({
  name: "Destination-Component",
  components: {
    DestinationImage,
    DestinationData,
  },
  data() {
    return {
      moon: true,
      mars: false,
      europa: false,
      titan: false,
    };
  },
  methods: {
    trocarEstacao(estacao: string) {
      this.moon = false;
      this.mars = false;
      this.europa = false;
      this.titan = false;

      if (estacao == "moon") {
        this.moon = true;
      } else if (estacao == "mars") {
        this.mars = true;
      } else if (estacao == "europa") {
        this.europa = true;
      } else {
        this.titan = true;
      }
      console.log(this.moon, this.mars, this.europa, this.titan);
    },
  },
});
</script>
