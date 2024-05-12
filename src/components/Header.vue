<script setup lang="ts">
</script>

<template>
<header>
  <router-link class="back-btn" to="/">aタグで同窓遷移</router-link>
  <router-link class="back-btn" to="/about">Window.scrollで同窓遷移</router-link>
</header>
</template>

<style scoped>
header {
  display: flex;
  align-items: center;
  justify-content: space-around;
  height: 3rem;
  position: fixed;
  top: 0;
  background-color: #fff;
  width: 100%;
}
a {
  color: black;
  font-weight: bold;
}
</style>
