<template>
  <div>
    <h1>Calculator</h1>
    <input type="number" v-model="num1" placeholder="Number 1">
    <input type="number" v-model="num2" placeholder="Number 2">
    <button @click="add">+</button>
    <button @click="subtract">-</button>
    <button @click="multiply">*</button>
    <button @click="divide">/</button>
    <h2>Result: {{ result }}</h2>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const num1 = ref(0);
    const num2 = ref(0);
    const result = ref(0);

    const add = () => {
      result.value = num1.value + num2.value;
    };

    const subtract = () => {
      result.value = num1.value - num2.value;
    };

    const multiply = () => {
      result.value = num1.value * num2.value;
    };

    const divide = () => {
      result.value = num1.value / num2.value;
    };

    return { num1, num2, result, add, subtract, multiply, divide };
  }
};
</script>

<style>
/* Add any styles for the calculator here */
</style>
