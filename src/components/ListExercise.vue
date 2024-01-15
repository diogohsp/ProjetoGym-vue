<script setup>
import { ref } from 'vue'
import Exercise from './Exercise.vue'

const serieAtual = ref(1)
const list = ref([])

const props = defineProps(['exercise'])

function add(){
    if(list.value.length < 6){
        list.value.push({serie: serieAtual.value})
        serieAtual.value++
    }
}
</script>

<template>
    <div class="w-[25vw] h-[32vw] bg-white rounded-[35px] ml-[2vw] shadow-lg shadow-slate-900 flex flex-col items-center">
        <h1 class="text-[2.5vw] font-poppins">{{ exercise }}</h1>
        <button @click="add" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full mb-[1vw]">
            Adicionar
        </button>
        <div class="bg-slate-300 w-[22vw] h-[4vw] rounded-[35px] flex items-center mb-[1vw] justify-evenly">
            <p class="text-[1.2vw]">Série</p>
            <p class="text-[1.2vw]">KG</p>
            <p class="text-[1.2vw]">Repetições</p>
            <p class="text-[1.2vw]">Status</p>
        </div>
        <Exercise class="mb-[1vw]" v-for="(item, index) in list" :key="index" :serie="item.serie"/>
    </div>
</template>

<style>

</style>