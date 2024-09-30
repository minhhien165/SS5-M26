<template>
    <div>
        <h1>Ex07</h1>
      <button
        v-for="(item, index) in data"
        :key="index"
        @click="handleButton(index)"
        :class="{ active: activeIndex === index }"
      >
        Button {{ item.id }}
      </button>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  
  const data = [
    { id: 1 },
    { id: 2 },
    { id: 3 },
  ];
  
  const activeIndex = ref(0); 
  
  const handleButton = (index) => {
    activeIndex.value = index; 
  };
  </script>
  
  <style>
  button {
    margin: 5px;
  }
  
  button.active {
    background-color: red;
    color: #fff;
  }
  </style>
  