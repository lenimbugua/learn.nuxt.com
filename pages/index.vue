<script setup lang="ts">
import '@unocss/reset/tailwind.css'

const { x, y } = useMouse()

const colorMode = useColorMode()

function toggleColorMode() {
  colorMode.value = colorMode.value === 'light'
    ? 'dark'
    : 'light'
}
</script>

<template>
  <div class="grid grid-cols-[1fr_2fr] h-full ">
    <div class="border-r border-base p4">
      <div class="text-red">
        <h1>Hello World {{ x }} {{ y }}</h1>
      </div>
      <button @click="toggleColorMode">
        {{ colorMode.value }}
      </button>
    </div>
    <div class="p4">
      <ThePlayground />
    </div>
  </div>
</template>

<style>
.dark-mode body {
  background-color: #091a28;
  color: #ebf4f1;
}
</style>
