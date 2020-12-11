<template>
  <div class="p-use">
    <!-- Tabela de resultados P-Uso -->
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
          <!-- Itera nos registros do P-Uso -->
          <tr v-for="variable in pUso.variaveis" :key="variable.name">
            <td>{{ variable.identificador }}</td>
            <td>{{ variable.valor }}</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="total-container">
      <!-- Total de P-Uso -->
      <h3 class="p-use-result">Total: {{ pUso.total }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  props: ["pUso"]
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