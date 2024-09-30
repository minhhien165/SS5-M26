<template>
  <div>
    <h1>condition & list rendering</h1>
    <ul>
      <li>V-IF</li>
      <li>V-ELSE</li>
      <li>V-ELSE-IF</li>
      <li>V-SHOW</li>
    </ul>
    <p>V-IF</p>
    <p v-if="isCheck">hiển thị v-if nếu điện thỏa mãn</p>
    <p v-else>đko ko thỏa mãn</p>
    <ul>
      <li  v-for="(student, id) in students" :key="student.id">
        {{id + 1}} {{student.name}}
      </li>
    </ul>
  </div>
</template>

<script setup>
const isCheck = false;
const students = [
  {
    id: 1,
    name: "Hồng Vân",
  },
  {
    id: 2,
    name: "Ánh Linh",
  },
  {
    id: 3,
    name: "Thảo Phương",
  },
];

</script>

<style>
</style>