<script setup>
import { ref } from 'vue'

const num1 = ref(0)
const num2 = ref(0)
const result = ref(0)
</script>

<template>
  <div class="calculator">
    <input type="number" v-model="num1">
    <button @click="result = num1 + num2">+</button>
    <button @click="result = num1 - num2">-</button>
    <button @click="result = num1 * num2">*</button>
    <button @click="result = num1 / num2">/</button>
    <input type="number" v-model="num2">
    <span>=</span>
    <input type="number" v-model="result">
  </div>
</template>

<style scoped>
.calculator {
  margin-top: 32px;
  display: flex;
  align-items: center;
  gap: 16px;
}

.calculator input {
  width: 100px;
  border: 1px solid #0000004d;
  outline: none;
  border-radius: 4px;
  padding: 8px;
}

.calculator button {
  border: none;
  outline: none;
  border-radius: 4px;
  padding: 8px 20px;
  background-color: coral;
  color: white;
}
</style>