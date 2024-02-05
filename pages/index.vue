<script setup lang="ts">
import "@unocss/reset/tailwind.css";
const { x, y } = useMouse();

const colorMode = useColorMode();

const toggleColorMode = () => {
  colorMode.value = colorMode.value === "light" ? "dark" : "light";
  return;
};

console.log(colorMode.value);
</script>
<template>
  <div class="text-red">
    <h1>Hello World {{ x }} {{ y }}</h1>
  </div>
  <button @click="toggleColorMode">{{ colorMode.value }}</button>
</template>

<style>
.dark-mode body {
  background-color: #091a28;
  color: #ebf4f1;
}
</style>
