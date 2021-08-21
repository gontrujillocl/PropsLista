<template>
  <div class="container">
    <h1 class="ml-3 mt-4">{{ nombre }}</h1>
    <Agregar @nueva-actividad="agregarNuevaActividad" />
    <Lista :actividades="actividades" />
  </div>
</template>

<script>
import Agregar from "./components/Agregar.vue";
import Lista from "./components/Lista.vue";
export default {
  name: "App",
  components: {
    Lista,
    Agregar,
  },
  data: () => ({
    nombre: "Cosas por hacer",
    actividades: [],
  }),

  methods: {
    agregarNuevaActividad(nuevaActividad) {
      this.actividades.push(nuevaActividad), (this.nuevaActividad = "");
    },
  },
};
</script>
