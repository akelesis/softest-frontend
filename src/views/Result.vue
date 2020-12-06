<template>
  <div class="result">
      <Header />
      <div class="tables-container">
        <VariableTable/>
        <div class="use-cases">
            <CUseResult/>
            <PUseResult />
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
    methods: {
        redirectHome() {
            this.$router.push("/")
        }
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