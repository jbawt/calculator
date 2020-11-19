<template>
  <div class="option-container">
    <Numbers v-bind:clear="clear" v-on:option="$emit('option', $event)" />
    <Operands v-on:answer="$emit('answer', $event)" v-on:operand="$emit('operand', $event)" />
  </div>
</template>

<script>
import Operands from './options/Operands';
import Numbers from './options/Numbers';

export default {
  name: "OptionContainer",
  props: ["clear"],
  components: {
    Operands,
    Numbers
  }
}
</script>

<style scoped>
  .option-container {
    width: 100%;
    height: 80%;
    border-bottom-left-radius: 10px;
    border-bottom-right-radius: 10px;
    display: flex;
  }
</style>