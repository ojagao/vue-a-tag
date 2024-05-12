<script setup lang="ts">
import { onMounted, ref } from 'vue';

const anchor = ref<HTMLElement | null>(null);

onMounted(() => {
  anchor.value = document.querySelector('#anchor');
});

const smoothScroll = () => {
  const element = anchor.value;
  if (element) {
    window.scrollTo({
      top: element.offsetTop,
      behavior: 'smooth'
    });
  }
}
</script>

<template>
  <div>
    <div class="page page1">
      <div>
        <p>buttonタグでclickイベントを使用して<br />JSでスクロール制御しています。</p>
        <button @click="smoothScroll">↓ Clickイベントです　</button>
      </div>
    </div>
    <div class="page page2">
      <p>2</p>
    </div>
    <div class="page page3">
      <p>3</p>
    </div>
    <div id="anchor"class="page page4">
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
  background: gray;
  display: grid;
  place-items: center;
  text-align: center;
}
button {
  background: #2b00ff;
  color: #fff;
  padding: 8px 16px;
  text-decoration: none;
  margin-top: 1rem;
  border-radius: 12px;
  display: block;
  width: 100%;
}
.page2 {
  background: rgb(255, 255, 255);
}
.page3 {
  background: gray;
}
.page4 {
  background: rgb(255, 255, 255);
}
</style>
