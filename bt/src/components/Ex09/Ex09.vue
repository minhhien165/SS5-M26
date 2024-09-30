<template>
    <div>
      <h1>Ex09</h1>
      <p>Giới tính hiện tại: {{ currentGender }}</p>
      <button @click="randomizeGender">Random Gender</button>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  
  const genders = ["Nam", "Nữ", "Khác"];
  
  const currentGender = ref("Nam");
  
  const randomizeGender = () => {
    const randomIndex = Math.floor(Math.random() * genders.length);
    currentGender.value = genders[randomIndex]; 
  };
  </script>
  
  <style>
  </style>
  