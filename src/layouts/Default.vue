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
          <p class="text-center text-xs text-gray-500 leading-5">
            &copy; {{ new Date().getFullYear() }} 闪电工作室 <a href="https://beian.miit.gov.cn">浙ICP备2024111886号-2</a>
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>
