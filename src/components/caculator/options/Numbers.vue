<template>
  <div class="numbers">
    <div v-on:click="clickOption" class="box">
      <h1>C</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>+/-</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>%</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>7</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>8</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>9</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>4</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>5</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>6</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>1</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>2</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>3</h1>
    </div>
    <div v-on:click="clickOption" class="box stretched bottom">
      <h1>0</h1>
    </div>
    <div v-on:click="clickOption" class="box">
      <h1>.</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "Numbers",
  props: ["clear"],
  methods: {
    clickOption(e) {
      if (e.target.childNodes[0].data === 'C') {
        let value = '';
        this.$emit('option', value);  
      } else {
      let value = e.target.childNodes[0].data
      this.$emit('option', value)
      }
    }
  }
}
</script>

<style scoped>
  .numbers {
    display: flex;
    width: 80%;
    height: 100%;
    flex-wrap: wrap;
  }

  .numbers .box {
    width: 33.33%;
    height: 20%;
    border-bottom: 2px solid black;
    display: flex;
    justify-content: center;
    align-items: center;
    border-left: 2px solid black;
    border-bottom: 2px solid black;
    cursor: pointer;
  }

  .bottom {
    border-bottom-left-radius: 10px;
  }

  .stretched {
    flex: 2;
  }
</style>