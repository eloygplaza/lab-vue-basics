<template>
<h1 class="is-size-1">Iteration 1</h1>
<h2>Componentes Navbar y Footer añadidos</h2>

<h1 class="is-size-1">Iteration 2</h1>
<h2>Mostar suma: "{ { 2 + 2 } }" = {{ 2 + 2 }}</h2>
<h2>Mostrar texto de una funcion: {{showString()}}</h2>
</template>

<script setup>
import { ref } from 'vue';

function showString (){
    return ref("Hola");
}
</script>

<style scoped>
</style>