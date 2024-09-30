<template>
    <div>
      <h1>Ex10</h1>
      <button @click="handleClick">Random number</button>
      <ul>
        <li v-for="(number, index) in randomNumbers" :key="index">
          {{ number }}
        </li>
      </ul>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  const randomNumbers = ref([]);
  
  const handleClick = () => {
    const randomNum = Math.floor(Math.random() * 100);
    randomNumbers.value.push(randomNum);
  };
  </script>
  
  <style>
  </style>
  