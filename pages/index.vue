<script setup>
const { x, y } = useMouse();

const colorMode = useColorMode();

console.log(colorMode.value);
</script>
<template>
  <div>
    <h1>Hello World {{ x }} {{ y }}</h1>
  </div>
  <button
    @click="colorMode.value = colorMode.value === 'light' ? 'dark' : 'light'"
  >
    Toggle Color mode
  </button>
</template>

<style>
.dark-mode body {
  background-color: #091a28;
  color: #ebf4f1;
}
</style>
