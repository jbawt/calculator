<template>
  <div class="operands">
    <div v-on:click="clickOption" class="box">
      <h1>/</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>*</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>-</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>+</h1>
    </div>
    <div v-on:click="clickOption" class="box bottom">
      <h1>=</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "Operands",
  methods: {
    clickOption(e) {
      let value = e.target.childNodes[0].data
      this.$emit('operand', value)
    }
  }
}
</script>

<style scoped>
  .operands {
    display: flex;
    flex-direction: column;
    border-left: 2px solid black;
    height: 100%;
    width: 20%;
  }

  .operands .box {
    width: 100%;
    height: 100%;
    border-bottom: 2px solid black;
    display: flex;
    justify-content: center;
    align-items: center;
    background: orange;
  }

  .bottom {
    border-bottom-right-radius: 10px;
  }
</style>