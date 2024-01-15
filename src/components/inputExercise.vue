<script setup>
    sendTitle() {
        $emit('sendTitle', texto)
    }
</script>

<template>
    <div class="bg-slate-300 w-[22vw] h-[4vw] rounded-[35px] flex items-center justify-evenly">
        <input type="text" :value="texto" placeholder="Nome do Exercicio" class="text-[1.2vw] rounded-xl text-center" keydown.enter="sendTitle">
    </div>
</template>


<style scoped>

</style>