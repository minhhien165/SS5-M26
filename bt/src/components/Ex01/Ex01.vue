<template>
  <div>
    <h1>Ex01</h1>

    <p v-show="isShow">Rikkei Education</p>
    <button @click="handleSubmit">Hiện</button>
  </div>
</template>
  
  <script setup>
import { ref } from "vue";

// Biến để kiểm soát hiển thị
const isShow = ref(false);
const handleSubmit = () => {
  isShow.value = true;
};
</script>
  
  <style>
</style>
  