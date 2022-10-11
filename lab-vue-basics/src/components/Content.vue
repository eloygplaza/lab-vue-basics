<template>
<h1 class="is-size-1">Iteration 1</h1>
<h2>Componentes Navbar y Footer añadidos</h2>

<h1 class="is-size-1">Iteration 2</h1>
<h2>Mostar suma: "{ { 2 + 2 } }" = {{ 2 + 2 }}</h2>
<h2>Mostrar texto de una funcion: {{showString()}}</h2>

<h1 class="is-size-1">Iteration 3</h1>
<h2 v-if="showText">Este texto es visible si su variable es true</h2>
</template>

<script setup>
import { ref } from 'vue';

function showString (){
    return ref("Hola");
}

let showText = true;
</script>

<style scoped>
</style>