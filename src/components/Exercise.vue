<script>
export default{
    props: ['serie'],
    data() {
        return {
            name: 'Supino',
            quantidade: 0,
            timer: 0,
        }
    },
    methods: {
        
    }
}
</script>

<template>
    <div class="bg-slate-300 w-[22vw] h-[4vw] rounded-[35px] flex items-center justify-evenly">
        <p>{{ serie }}</p>
        <input type="text" placeholder="KG" class=" text-[1.2vw] w-[3vw] h-[2vw] rounded-md text-center">
        <input type="number" placeholder="Reps" class="w-[6vw] h-[2vw] rounded-md text-center">
        <input type="checkbox">
    </div>
</template>

<style>

</style>
