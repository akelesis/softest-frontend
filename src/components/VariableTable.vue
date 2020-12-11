<template>
  <div class="variable-table">
    <!-- Tabela de resultados de Variáveis -->
    <h2>VARIÁVEIS</h2>
    <div class="table-container">
      <table>
        <thead>
          <tr>
            <td>IDENTIFICADORES</td>
            <td>TIPOS</td>
            <td>DEF</td>
            <td>ULTIMO USO</td>
          </tr>
        </thead>
        <tbody>
          <!-- Itera nos registros do C-Uso -->
          <tr v-for="variable in cUso.variaveis" :key="variable.name">
            <td>{{ variable.identificador }}</td>
            <td>{{ variable.tipo }}</td>
            <td>{{ variable.def }}</td>
            <td>{{ variable.ultimoUso }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  props: ["cUso"]
};
</script>

<style>
.table-container {
  border: 1px solid #a4a4a4;
  width: 100%;
  height: 620px;
}

.variable-table {
  width: 600px;
  font-family: "Roboto", sans-serif;
}

.variable-table h2 {
    font-weight: 300;
}

.variable-table table {
  width: 100%;
}

.variable-table tr {
  border-bottom: 1px solid #a4a4a4;
}
</style>