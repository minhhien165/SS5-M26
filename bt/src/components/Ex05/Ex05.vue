<template>
  <div>
    <h1>Ex05</h1>
    <button @click="handleIncrease">Tăng</button>
    <button @click="handleDecrease">Giảm</button>
    <ul>
      <li v-for="num in filteredEvenNumbers" :key="num">{{ num }}</li>
    </ul>
  </div>
</template>
  
  <script setup>
import { ref, computed } from "vue";

const integerArray = ref([1, 4, 2, 3, 5, 8, 7, 6]);
const order = ref("increase");

const filteredEvenNumbers = computed(() => {
  const evens = integerArray.value.filter((num) => num % 2 === 0);
  return order.value === "increase"
    ? evens.sort((a, b) => a - b)
    : evens.sort((a, b) => b - a);
});

const handleIncrease = () => {
  order.value = "increase";
};

const handleDecrease = () => {
  order.value = "decrease";
};
</script>
  
  <style>
</style>
  