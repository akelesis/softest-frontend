<template>
  <div class="c-use">
    <h2>RESULTADO C-USO</h2>
    <div class="table-container">
      <table>
        <thead>
          <tr>
            <td>VARIAVEL</td>
            <td>VALOR</td>
          </tr>
        </thead>

        <tbody>
          <tr v-for="variable in variables" :key="variable">
            <td>{{ variable.name }}</td>
            <td>{{ variable.value }}</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="total-container">
      <h3 class="c-use-result">Total: {{ total }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      variables: [
        {
          name: "contador",
          value: 45,
        },
      ],
      total: 45,
    };
  },
};
</script>

<style>
.c-use .table-container {
  width: 300px;
}

.c-use .table-container table {
  width: 300px;
}

.c-use {
  width: 300px;
}

.total-container {
    width: 100%;
    border: 1px solid #a4a4a4;
}

.c-use h2 {
  font-weight: 300;
}
</style>