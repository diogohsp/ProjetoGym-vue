<script setup>
import { ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router'

import Header from './components/Header.vue'
import InputExercise from './components/inputExercise.vue'
import ListExercise from './components/ListExercise.vue'
import Footer from './components/Footer.vue'

const valueReceive = ref('')

function receiveValueTitle(value){
    valueReceive.value = value
}

</script>

<template>
  <div class="bg-gradient-to-br from-cor1bg to bg-cor2bg">
    <div class="flex flex-col justify-center items-center h-screen w-full">

    <Header class="absolute top-0"/>
    <InputExercise  @sendTitle="receiveValueTitle" />
    <ListExercise class="mt-6" :title="valueReceive" :exercise="exercise"/>
    <Footer class="absolute bottom-0"/>
  
    </div>

  </div>
  
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
