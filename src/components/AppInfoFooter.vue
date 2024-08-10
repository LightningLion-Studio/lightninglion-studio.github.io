<script setup lang="tsx">
defineProps({
  developer: String,
  version: String,
  releaseDate: {
    type: String,
    default: new Date().toLocaleDateString(),
  },
})
</script>

<template>
  <div ml2 mt2 flex flex-wrap gap-x3 font-size-3 op-30>
    <span>开发者：{{ developer }}</span>
    <span>版本号：{{ version }}</span>
    <span>发布时间：{{ releaseDate }}</span>
    <span cursor-pointer border-b="1 solid red-200" hover:border-b="2 solid yellow-300">应用权限</span>
    <span cursor-pointer border-b="1 solid red-200" hover:border-b="2 solid yellow-300">隐私政策</span>
  </div>
</template>
