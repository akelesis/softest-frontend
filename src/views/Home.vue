<template>
  <div class="home">
    <Header />
    <div class="content-container">
      <Description />
      <CodeInput />
    </div>
  </div>
</template>

<script>
import Description from '../components/Description'
import Header from '../components/Header'
import CodeInput from '../components/CodeInput'

export default {
  name: 'Home',
  components: {
    Description,
    Header,
    CodeInput
  }
}
</script>

<style>
  .home {
    width: 70vw;
  }

  .content-container {
    display: flex;
    justify-content: space-between;
  }
</style>