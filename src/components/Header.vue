<template>
  <div class="header">
    <h1>Calculator App</h1>
    <p>Josh Bawtinheimer</p>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  width: 100%;
  height: 15vh;
  border-bottom: 2px solid black;
  background-color: rgba(49, 148, 102, 0.898);
  display: flex;
  justify-content: center;
  align-items: center;
}

.header h1 {
  flex-grow: 2;
  text-align: center;
  position: relative;
  left: 7vw;
  font-weight: 1500;
  font-size: 3em;
}

.header p {
  margin-right: 1vw;
  font-weight: bold;
}
</style>
