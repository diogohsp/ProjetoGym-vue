<script setup>
import Exercise from './Exercise.vue'

</script>


<script>

export default{
    data(){
        return{
            list: [],
        }
    },

    methods: {
        add(){
            if(this.list.length < 8){
                return this.list.push({})
            }
        }
    }
}
</script>

<template>
    <div class="w-[25vw] h-[32vw] bg-white rounded-[35px] ml-[2vw] shadow-lg shadow-slate-900 flex flex-col items-center">
        <h1 class="text-[2.5vw] font-poppins">Exercise</h1>
        <button @click="add" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full mb-[1vw]">
            Adicionar
        </button>
        <Exercise class="mb-[1vw]" v-for="(item, index) in list" :key="index"/>
    </div>
</template>

<style>

</style>