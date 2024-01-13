<script>
export default{
    data() {
        return {
            name: 'Supino',
            quantidade: 0,
            timer: 0,
        }
    }
}
</script>

<template>
    <div class="bg-slate-300 w-[22vw] h-[4vw] rounded-[35px] flex items-center">
        <h1 class="text-[1vw] font-poppins">Exercicio: {{ name }} Repetições: {{ quantidade }}</h1>
    </div>
</template>

<style>

</style>
