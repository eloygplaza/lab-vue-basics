<template>
<h1 class="is-size-1">Iteration 1</h1>
<h2>Componentes Navbar y Footer añadidos</h2>

<h1 class="is-size-1">Iteration 2</h1>
<h2>Mostar suma: "{ { 2 + 2 } }" = {{ 2 + 2 }}</h2>
<h2>Mostrar texto de una funcion: {{showString()}}</h2>

<h1 class="is-size-1">Iteration 3</h1>
<h2 v-if="showText">Este texto es visible si su variable es true</h2>

<h1 class="is-size-1">Iteration 4</h1>
<ul>
    <li v-for="post in posts"><b>Title</b>: {{post.title}} // <b>Description</b>: {{post.description}} // <b>Content</b>: {{post.content}}</li>
</ul>

</template>
<!-- END TEMPLATE -->

<!-- START SCRIPT -->
<script setup>
import { ref } from 'vue';

function showString (){
    return ref("Hola");
}

let showText = true;

let posts = [
    {
        title: "Unseen Tribunal",
        description: "Attack of Mars",
        content: "The Speckled Statue"
    },
    {
        title: "The Dance of the Raven",
        description: "Devil's Voyage",
        content: "Throne and the Shield"
    },
    {
        title: "The Crooked Sun",
        description: "The Owl in the Mist",
        content: "Hiddne Midnight"
    }
];
</script>

<style scoped>
</style>