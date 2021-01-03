<template>
    <div>
        <h1>{{tituloBanco}}</h1>
    <h2>Bienvenido, {{nombreUser}}</h2>
    </div>
</template>

<script>
export default {
    name: 'Titulo',
    props: {
        tituloBanco: String
    },
    data(){
        return{
            nombreUser:'Leonardo Navarro'
        }
    }
}
</script>

<style>

</style>
/* Este componente sera llamado como Props desde App */