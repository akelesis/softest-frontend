<template>
  <div class="variable-table">
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
          <tr v-for="variable in variables" :key="variable">
            <td>{{ variable.name }}</td>
            <td>{{ variable.type }}</td>
            <td>{{ variable.def }}</td>
            <td>{{ variable.lastUse }}</td>
          </tr>
        </tbody>
      </table>
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
          type: "int",
          def: 5,
          lastUse: 45,
        },
      ],
    };
  },
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