<script setup lang="tsx">
defineProps({
  size: {
    type: Number,
    default: 700,
  },
  src: String,
  height: {
    type: Number,
  },
  width: {
    type: Number,
  },
})
</script>

<template>
  <div
    class="bg absolute bg-no-repeat op-5 dark:op-30 dark:filter-invert-1"
    :style="{ width: `${width ?? size}px`, height: `${height ?? size}px`, backgroundImage: `url(${src})`, backgroundSize: `${size}px` }"
  />
</template>

<style lang="less" scoped>
.bg {
  mask: linear-gradient(to right, rgb(255 0 0), rgb(0 0 255));
}
</style>
