<template>
    <button  @click="onClick()" :style="{background: color}" class="btn">{{text}}</button>    
</template>

<script>
    export default{
        name: 'AppButton',
        props: ['text','color'],
        methods: {
            onClick(){
                this.$emit('btn-click')
            }
        }
    }
</script>

<style scoped>

</style>