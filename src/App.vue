<template >
  <div class="container text-center">
  <img class="mt-4" alt="Vue logo" src="./assets/download.png">
  <!-- Titulo -->
    <Titulo tituloBanco="Mi Banco en línea"/>
    <!-- Contenido de cuenta -->
    <Cuenta/>
    <!-- Botones -->
    

    
  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue' */
import Titulo from './components/Titulo'
import Cuenta from './components/Cuenta'


export default {
  name: 'App',
  components: {
    Titulo, 
    Cuenta
    
  }
}
</script>

<style>

</style>
