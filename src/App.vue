<script setup>
import { ref } from 'vue'

const getRandomInt = max => Math.floor(Math.random() * max)
const number = ref(1)
</script>

<template>
  <main
    class="
      space-y-7
      max-w-full max-h-full
      flex flex-col
      items-center
      justify-center
      h-screen
    "
  >
    <img
      class="
        rounded-lg
        object-cover
        h-96
        aspect-video
      "
      :src="`https://chubarich.fvs.app/${number}.png`"
    >

    <button
      class="
        text-lg
        font-medium
        py-2
        px-4
        rounded-md
        text-white
        bg-blue-600
        shadow-md
        shadow-blue-500/50
        hover:bg-blue-700
      "
      @click="number = getRandomInt(32)"
    >
      Новый Чубарыч
    </button>
  </main>
</template>

<style scoped>
</style>
