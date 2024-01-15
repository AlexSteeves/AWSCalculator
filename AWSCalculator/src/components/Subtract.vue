<template>
    <div>
      <input v-model.number="operand1" type="number" placeholder="Number 1" />
      <input v-model.number="operand2" type="number" placeholder="Number 2" />
      <button @click="subtract">Subtract</button>
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
      subtract() {
        this.$emit('result', this.operand1 - this.operand2);
      },
    },
  };
  </script>
  