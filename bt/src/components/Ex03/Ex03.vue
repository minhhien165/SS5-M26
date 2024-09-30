<template>
  <div>
    <h1>Ex03</h1>
    <p v-if="userRole === admin">quyền hạn của bạn là:admin</p>
    <p v-else-if="userRole === user">quyền hạn của bạn là:user</p>
    <p v-else-if="userRole === guest">quyền hạn của bạn là:guest</p>
  </div>
</template>
  
  <script setup>
const userRole = "admin";
</script>
  
  <style></style>