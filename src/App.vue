<script setup>
import { ref } from "vue";

const getRandomInt = (max) => Math.floor(Math.random() * max);
const number = ref(1);
</script>

<template>
  <main
    class="
      space-y-7
      py-40
      max-w-full max-h-full
      flex flex-col
      items-center
      justify-center
      bg-scroll
      h-100
      w-100
      bg-slate-200
    "
  >
    <img
      class="
        rounded-lg
        mt-6
        space-y-4
        object-center
        h-100
        w-100
        max-w-80 max-h-80
        items-center
        justify-center
      "
      :src="`https://chubarich.fvs.app/${number}.png`"
    />

    <button
      class="
        text-lg
        pt-1
        space-y
        h-10
        w-40
        rounded-md
        border-black
        text-white
        bg-blue-600
        shadow-md
        object-center
      "
      @click="number = getRandomInt(32)"
    >
      Новый Чубарыч
    </button>
  </main>
</template>

<style scoped>
</style>