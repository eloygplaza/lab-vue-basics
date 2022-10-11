<!-- START TEMPLATE -->
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
    <li v-for="post in posts" :key="post.title"><b>Title</b>: {{post.title}} // <b>Description</b>: {{post.description}} // <b>Content</b>: {{post.content}}</li>
</ul>

<h1 class="is-size-1">Iteration 5</h1>
<button @click="changeColor()">Click to change color</button>
<h2 :class="[isActive ? 'red' : 'blue']">H2 change background color on each click</h2>
</template>
<!-- END TEMPLATE -->

<!-- START SCRIPT -->
<script setup>
import { ref } from 'vue';

// ITERATION 2
function showString (){
    return ref("Hola");
}

// ITERATION 3
let showText = true;

// ITERATION 4
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

// ITERATION 5 
let isActive = ref(true);

function changeColor() {
    isActive.value = !isActive.value;
}
</script>
<!-- END SCRIPT -->

<!-- START STYLE -->
<style scoped>
.red{
  background: red;
}

.blue{
  background: blue;
}
</style>
<!-- END STYLE -->