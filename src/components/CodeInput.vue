<template>
  <div class="code-input">
    <textarea id="code-textarea" cols="30" rows="10"></textarea>
    <button class="default-button" @click="redirectResult">EXECUTAR</button>
  </div>
</template>

<script>
export default {

    methods: {
        redirectResult() {
            this.$router.push("Result")
        }
    }
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
  transition: .2s;
}

.default-button:hover{
  background-color: #7bc097;
  cursor: pointer;
}
</style>