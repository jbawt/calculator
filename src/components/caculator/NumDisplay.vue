<template>
  <div class="num-display">
    <h2>{{options}}</h2>
  </div>
</template>

<script>
export default {
  name: "NumDisplay",
  props: ["options"]
}
</script>

<style scoped>
.num-display {
  width: 100%;
  height: 20%;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  background: black;
  color: white;
}
</style>