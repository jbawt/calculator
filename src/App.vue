<template>
  <div class="app">
    <Header />
    <Container />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Container from './components/caculator/Container'

export default {
  name: 'App',
  components: {
    Header,
    Container
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Courier New', Courier, monospace;
  line-height: 1.2em;
}

.app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
