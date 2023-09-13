<script>
// import Saludo from "@/components/Saludo.vue";
import Maquina from "@/components/Maquina.vue"
import Rain from "@/components/Rain.vue"
export default {
  components: {
    
    // Saludo,
    Maquina,
    Rain
  }
};
</script>

<template>
    <div>
        
      <!-- <Saludo /> -->
        <Maquina />
        <h2 class="text-white text-xl ml-6">Acerca de mi</h2>
        <Rain />
    </div>
  </template>