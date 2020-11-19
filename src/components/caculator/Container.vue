<template>
  <div class="calc-div">
    <NumDisplay v-bind:options="options" />
    <OptionContainer v-on:option="addOptions($event)" v-on:operand="addOptions($event)"/>
  </div>
</template>

<script>
import NumDisplay from './NumDisplay';
import OptionContainer from './OptionContainer';

export default {
  name: "Calculator",
  data() { 
    return {
      options: ''
    } 
  },
  components: {
    NumDisplay,
    OptionContainer
  },
  methods: {
    addOptions(option) {
      if (option === '') {
        this.options = '';
      } else {
        this.options += option;
      }
    }
  }
}
</script>

<style scoped>
  .calc-div {
    width: 25vw;
    height: 60vh;
    display: flex;
    flex-direction: column;
    justify-self: center;
    align-self: center;
    margin-top: 2em;
    border-radius: 10px;
    box-shadow: 0px 5px 5px 5px rgb(119, 119, 119), 0px 15px 15px 15px rgb(163, 163, 163);
  }
</style>