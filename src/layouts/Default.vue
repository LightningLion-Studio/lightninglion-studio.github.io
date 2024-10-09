<script setup lang="tsx"></script>

<template>
  <div light:bg-white dark="from-[bg-gray-900] to-[transparent]">
    <div class="pointer-events-none fixed inset-0 select-none bg-[url(./grid-black.svg)] bg-top bg-repeat dark:bg-[url(/grid.svg)]" op-90 dark:op-30 />
    <header absolute inset-x-0 top-0 z-50>
      <nav class="mx-auto max-w-7xl flex items-center justify-between" p="6 x6" lg:p="x8" aria-label="Global">
        <div>
          <img src="../assets/favicon.png" class="h8 w-auto">
        </div>
        <div>
          <button @click="toggleDark()">
            <div font-size-4.5 :class="isDark ? 'i-ph-sun-duotone' : 'i-ph-moon-duotone'" />
          </button>
        </div>
      </nav>
    </header>
    <RouterView />
    <footer>
      <div class="mx-auto max-w-7xl px-6 py-12 md:flex md:items-center md:justify-between lg:px-8">
        <div class="flex justify-center md:order-2 space-x-6">
          <a href="https://github.com/LightningLion-Studio" class="text-gray-400 hover:text-gray-500">
            <span class="sr-only">GitHub</span>
            <div i-carbon-logo-github font-size-5 />
          </a>
        </div>
        <div class="mt-8 md:order-1 md:mt-0">
          <p class="text-xs text-gray-500 leading-5">
            &copy; {{ new Date().getFullYear() }} 闪电工作室 <a href="https://beian.miit.gov.cn">浙ICP备2024111886号-2</a> 腕上浏览器 <a href="https://beian.miit.gov.cn">浙ICP备2023001434号-4A</a>
            <br>
            <a href="https://www.yuque.com/u2182801/yehuom/dlse4xx3y0pc32k2?#%E3%80%8A%E8%85%95%E4%B8%8A%E6%B5%8F%E8%A7%88%E5%99%A8%20-%20%E6%9D%83%E9%99%90%E8%AF%B4%E6%98%8E%E6%96%87%E6%A1%A3%E3%80%8B">腕上浏览器权限说明</a>&nbsp;
            <a href="https://www.yuque.com/u2182801/yehuom/bow91oipabuc0l85?#%E3%80%8A%E8%85%95%E4%B8%8A%E6%B5%8F%E8%A7%88%E5%99%A8%E9%9A%90%E7%A7%81%E6%94%BF%E7%AD%96%E3%80%8B">腕上浏览器隐私政策</a>&nbsp;
            <a href="https://www.yuque.com/u2182801/lmrzrc/vkm4yacm7xuytwyt?singleDoc#%20%E3%80%8A%E6%82%A6%E9%9F%B3%E9%9F%B3%E4%B9%90%E9%9A%90%E7%A7%81%E6%94%BF%E7%AD%96%E3%80%8B">悦音音乐隐私政策</a>&nbsp;
            <a href="https://www.yuque.com/u2182801/lmrzrc/bxzr2fibvd6yl485?singleDoc#%20%E3%80%8A%E6%82%A6%E9%9F%B3%E9%9F%B3%E4%B9%90%E6%9D%83%E9%99%90%E8%AF%B4%E6%98%8E%E3%80%8B">悦音音乐权限说明</a>&nbsp;
            <a href="https://cd.darock.top:32767/meowbili/privacy/#/">喵哩喵哩隐私政策</a>
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>
