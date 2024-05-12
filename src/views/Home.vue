<script setup lang="ts">
const smoothScroll = () => {
  document.documentElement.style.scrollBehavior = 'smooth';
  setTimeout(() => {
    document.documentElement.style.scrollBehavior = 'auto';
  }, 100);
}
</script>

<template>
  <div>
    <div class="page page1">
      <div>
        <p>aタグでページ内遷移させています</p>
        <a @click="smoothScroll" href="#anchor">↓ aタグです　</a>
      </div>
    </div>
    <div class="page page2">
      <p>2</p>
    </div>
    <div class="page page3">
      <p>3</p>
    </div>
    <div id="anchor" class="page page4">
      <p>4</p>
    </div>
  </div>
</template>

<style scoped>
.page {
  width: 100%;
  height: calc(100vh - 3rem);
}
.page1 {
  background: rgb(119, 255, 82);
  display: grid;
  place-items: center;
  text-align: center;
}
a {
  background: #000;
  color: #fff;
  padding: 8px 16px;
  text-decoration: none;
  margin-top: 1rem;
  border-radius: 12px;
  display: block;
}
.page2 {
  background: rgb(255, 255, 255);
}
.page3 {
  background: rgb(119, 255, 82);
}
.page4 {
  background: rgb(255, 255, 255);
}
</style>
