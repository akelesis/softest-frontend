<template>
  <div class="p-use">
    <h2>RESULTADO P-USO</h2>
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
      <h3 class="p-use-result">Total: {{ total }}</h3>
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
          value: 84,
        },
      ],
      total: 84
    };
  },
};
</script>

<style>
.p-use .table-container {
  width: 300px;
}

.p-use .table-container table {
  width: 300px;
}

.p-use {
  width: 300px;
}

.p-use h2 {
  font-weight: 300;
}
</style>