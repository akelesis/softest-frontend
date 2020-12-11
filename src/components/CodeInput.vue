<template>
  <div class="code-input">
    <!-- Caixa de texto para enviar o código -->
    <textarea id="code-textarea" cols="30" rows="10"></textarea>
    <button class="default-button" @click="getResult">EXECUTAR</button>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      resultado: {},
    };
  },
  methods: {
    /* Função de redirecionamento para a pagina de resultados */
    redirectResult() {
      this.$router.push("Result");
    },
    /* Função que se comunica com o backend e recebe os dados*/
    async getResult() {
      this.resultado = await axios
        .post("http://localhost:3333/parser")
        .then((res) => res.data);

      if (this.resultado) {
        /* Guarda informação recebida do backend no localStorage do browser */
        localStorage.setItem("__cUso", JSON.stringify(this.resultado.cUso));
        localStorage.setItem("__pUso", JSON.stringify(this.resultado.pUso));
        this.redirectResult();
      }
    },
  },
};
</script>

<style>
.code-input {
  width: 50%;
}

#code-textarea {
  width: 100%;
  height: 700px;
  box-sizing: border-box;
  padding: 10px;
  resize: none;
  border-color: #a4a4a4;
  outline-color: #a4a4a4;
  font-family: monospace;
  color: #888;
}

.default-button {
  height: 60px;
  width: 100%;
  background-color: #96e0b4;
  border: none;
  color: #fff;
  transition: 0.2s;
}

.default-button:hover {
  background-color: #7bc097;
  cursor: pointer;
}
</style>