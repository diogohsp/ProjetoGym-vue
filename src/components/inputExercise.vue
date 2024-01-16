<script setup>
    import { ref } from 'vue'
    
    const title = ref('')

    const emit = defineEmits(['sendTitle']);

    function sendTitle() {
        emit('sendTitle', title.value)
    }

</script>

<template>
    <div class="bg-slate-300 w-[22vw] h-[4vw] rounded-[35px] flex items-center justify-evenly">
        <input type="text" placeholder="Nome do Exercicio" v-model="title" class="text-[1.2vw] rounded-xl text-center">
        <button @click="sendTitle" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Add</button>
    </div>
</template>


<style scoped>

</style>