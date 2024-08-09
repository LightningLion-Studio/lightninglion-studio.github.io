<script setup lang="ts">
import { darkTheme } from 'naive-ui'

// https://github.com/vueuse/head
// you can use this to manipulate the document head in any components,
// they will be rendered correctly in the html results with vite-ssg
useHead({
  title: 'Apple Watch 腕上系列',
  meta: [
    // {
    //   name: 'description',
    //   content: '',
    // },
    {
      name: 'theme-color',
      content: () => isDark.value ? '#00aba9' : '#ffffff',
    },
  ],
  link: [
    {
      rel: 'icon',
      type: 'image/svg+xml',
      href: '/favicon.png',
    },
  ],
})
</script>

<template>
  <NConfigProvider :theme="isDark ? darkTheme : null">
    <RouterView />
  </NConfigProvider>
</template>
