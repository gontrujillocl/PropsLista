<template>
  <div class="container my-4">
    <input
      class="form-control mb-2"
      @keyup.enter="agregarNuevaActividad"
      v-model="nuevaActividad"
      placeholder="Escribe para añadir a la lista..."
      type="text"
    />
    <button class="btn btn-warning" @click="agregarNuevaActividad">
      Añadir
    </button>
  </div>
</template>

<script>
export default {
  name: "Agregar",
  data: () => ({
    nuevaActividad: "",
  }),

  methods: {
    agregarNuevaActividad() {
      this.$emit("nueva-actividad", this.nuevaActividad);
      this.nuevaActividad = "";
    },
  },
};
</script>
