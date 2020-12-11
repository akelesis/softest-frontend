<template>
  <div class="c-use">
    <!-- Tabela de resultados C-Uso -->
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
          <!-- Itera nos registros do C-Uso -->
          <tr v-for="variable in cUso.variaveis" :key="variable.name">
            <td>{{ variable.identificador }}</td>
            <td>{{ variable.valor }}</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="total-container">
      <!-- Total do C-Uso -->
      <h3 class="c-use-result">Total: {{cUso.total }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  props: ["cUso"],
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