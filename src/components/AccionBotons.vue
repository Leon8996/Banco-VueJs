<template>
    <button  @click="accion" :disabled="desactivar"> {{textoBtn}} </button>
</template>

<script>
export default {
    name: 'AccionBotons',
    props: {
        textoBtn: String,
        desactivar:{
            type:Boolean,
            default: false

        } 

    },
    methods:{
        accion(){
            this.$emit('accion')
        }
    }
}
</script>

<style>

</style>