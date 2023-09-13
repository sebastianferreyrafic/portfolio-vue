<template>
  <div class="flex justify-center items-center ">
    <div class="font-extrabold text-xl m-5 inline-block border border-gray-300 p-2" id="saludo-container">{{ mensaje }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      saludo: ["B","I","E","N","V","E","N","I","D","@"],
      index: 0,
      mensaje: "",
      intervalo: null,
    };
  },
  created() {
    this.mostrarLetra();
    this.intervalo = setInterval(this.mostrarLetra, 300);
  },
  methods: {
    mostrarLetra() {
      if (this.index < this.saludo.length) {
        this.mensaje += this.saludo[this.index];
        this.index++;
      } else {
        this.index = 0;
        this.mensaje = "";
      }
    },
  },
  beforeDestroy() {
    clearInterval(this.intervalo);
  },
};
</script>
<style scoped>
#saludo-container {
  font-family: 'Josefin Sans', sans-serif;
  font-family: 'Kanit', sans-serif;
  font-family: 'Montserrat', sans-serif;
}
</style>