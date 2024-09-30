<template>
  <div>
    <h1>Ex02</h1>
    <button @click="handleIsShow">{{ isShow ? "Ẩn" : "Hiện" }}</button>
  </div>
</template>
  
  <script setup>
import { ref } from "vue";

const isShow = ref(false);

const handleIsShow = () => {
  isShow.value = !isShow.value;
};
</script>
  
  <style>
</style>
  