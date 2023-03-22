<template>
  <div class="container-data">
    <section class="esquerda"></section>
    <section class="direita">
      <div>
        <header>
          <nav class="navegacao-controle">
            <button>
              <h2 class="title-button">moon</h2>
            </button>
            <button>
              <h2 class="title-button">mars</h2>
            </button>
            <button>
              <h2 class="title-button">europa</h2>
            </button>
            <button>
              <h2 class="title-button">titan</h2>
            </button>
          </nav>
        </header>
      </div>
    </section>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Destination-Component",
});
</script>

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
  color: #ffffff;
  cursor: pointer;
  border-bottom: 4px solid white;
  padding-bottom: 10px;
  font-weight: 600;
}
</style>
