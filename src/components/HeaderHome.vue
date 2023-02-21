<template>
    <nav class="nav-header">
        <button class="botoes-header">
            <p class="numero=header">00 </p>
            <p class="descricao-header">Home</p>
        </button>
        <button class="botoes-header">
            <p class="numero=header">01 </p>
            <p class="descricao-header">Destination</p>
        </button>
        <button class="botoes-header">
            <p class="numero=header">02 </p>
            <p class="descricao-header">Crew</p>
        </button>
        <button class="botoes-header">
            <p class="numero=header">03 </p>
            <p class="descricao-header">Technology</p>
        </button>
    </nav>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: 'HeaderHome',

})
</script>
