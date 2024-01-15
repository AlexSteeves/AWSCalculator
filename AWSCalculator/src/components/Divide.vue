<template>
    <div>
      <input v-model.number="operand1" type="number" placeholder="Number 1" />
      <input v-model.number="operand2" type="number" placeholder="Number 2" />
      <button @click="divide">Divide</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        operand1: 0,
        operand2: 1, // Default to 1 to avoid division by zero
      };
    },
    methods: {
      divide() {
        if (this.operand2 !== 0) {
          this.$emit('result', this.operand1 / this.operand2);
        } else {
          alert('Cannot divide by zero.');
        }
      },
    },
  };
  </script>
  