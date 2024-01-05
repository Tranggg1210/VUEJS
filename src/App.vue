<script setup>
import { ref } from 'vue';
import Header from '@/components/Header.vue'

let a = ref(1);
const c = "hello";
const disable = ref(false);
const handleClick = () => {
  a.value++;
  if (a == 10) {
    disable.value = true;
    a.value = 0;
  };
}
</script>

<template>
  <h1 :class="c" :style="{
    padding: 20
  }">{{ a }}</h1>
  <button @click="handleClick" :disabled="disable">Click me</button>
  <Header />
</template>

<style scoped>
.hello {
  background-color: green;
  color: #fff;
  display: block;
}
</style>
