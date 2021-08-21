<template>
  <div class="container">
    <table class="table table-bordered table-dark">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Listado</th>
          <th scope="col">Borra lo realizado</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(actividad, index) in actividades" :key="index">
          <th scope="row">💪</th>
          <td>{{ actividad }}</td>
          <td>
            <button class="btn btn-danger" @click="eliminar(index)">
              Realizado 👌
            </button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "Lista",
  props: {
    actividades: { type: Array, required: true },
  },

  methods: {
    eliminar: function(index) {
      this.actividades.splice(index, 1);
    },
  },
};
</script>
