<template>
  <div class="result">
      <Header />
      <div class="tables-container">
        <VariableTable :cUso="cUso" />
        <div class="use-cases">
            <CUseResult :cUso="cUso" />
            <PUseResult :pUso="pUso" />
        </div>
      </div>
      <button class="default-button" @click="redirectHome">RETORNAR</button>
  </div>
</template>

<script>
import Header from "../components/Header"
import VariableTable from "../components/VariableTable"
import CUseResult from "../components/CUseResult"
import PUseResult from "../components/PUseResult"

export default {
    components: {
        Header,
        VariableTable,
        CUseResult,
        PUseResult
    },
    data() {
        return {
            resultado: {},
            pUso: {},
            cUso: {}
        }
    },
    methods: {
        redirectHome() {
            this.$router.push("/")
        },
        async getResult() {
            this.pUso = JSON.parse(localStorage.getItem("__pUso"))
            this.cUso = JSON.parse(localStorage.getItem("__cUso"))

            console.log(this.cUso)
            console.log(this.pUso)
        }
    },
    mounted() {
        this.getResult()
    }
}
</script>

<style>

.tables-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

.tables-container .use-cases {
    display: flex;
    justify-content: flex-end;
}

.result {
    width: 80vw;
}

.default-button {
    margin-top: 50px;
    margin-bottom: 50px;
}

</style>