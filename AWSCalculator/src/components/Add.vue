<template>
    <div>
      <input v-model.number="operand1" type="number" placeholder="Number 1" />
      <input v-model.number="operand2" type="number" placeholder="Number 2" />
      <button @click="add">Add</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        operand1: 0,
        operand2: 0,
      };
    },
    methods: {
      add() {
        this.$emit('result', this.operand1 + this.operand2);
      },
    },
  };
  </script>
  