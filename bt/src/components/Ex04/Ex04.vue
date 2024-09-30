<template>
  <div>
    <h1>Ex04</h1>
    <button @click="handleActive">Hiển thị</button>
    <button @click="handleUnActive">Ẩn</button>
    <p v-show="isVisible">Thông báo: Welcome to Rikkei Education</p>
  </div>
</template>
  
  <script setup>
import { ref } from "vue";

const isVisible = ref(false);

const handleActive = () => {
  isVisible.value = true;
};

const handleUnActive = () => {
  isVisible.value = false;
};
</script>
  
  <style>
</style>
  