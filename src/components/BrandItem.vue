<script setup lang="tsx">
defineProps({
  src: String,
  name: String,
})
</script>

<template>
  <div flex cursor-pointer gap3>
    <img class="max-h-15 w-auto rounded-full" :src="src" :alt="name" width="105" height="48" transition-all hover:transform-scale-110>
    <h3 class="mt-4 text-lg text-gray-900 font-semibold dark:text-white">
      {{ name }}
    </h3>
  </div>
</template>
