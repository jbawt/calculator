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
     <div v-on:click="equals" class="box bottom">
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
    },
    equals(e) {
      const operation = e.path[4].childNodes[0].childNodes[0].innerHTML;
      let inputs = operation.split(/[-/+*]/);
      let answer;
      if (operation.includes('+')) {
        answer = (Number(inputs[0]) + Number(inputs[1])).toString();
      }
      if (operation.includes('/')) {
        answer = (Number(inputs[0]) / Number(inputs[1])).toString();
      }
      if (operation.includes('*')) {
        answer = (Number(inputs[0]) * Number(inputs[1])).toString();
      }
      if (operation.includes('-')) {
        answer = (Number(inputs[0]) - Number(inputs[1])).toString();
      }
      this.$emit('answer', answer)
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
    cursor: pointer;
  }

  .bottom {
    border-bottom-right-radius: 10px;
  }
</style>