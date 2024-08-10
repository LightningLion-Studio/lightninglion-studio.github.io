<script setup lang="tsx">
const browserFeatures = [
  {
    name: '播放视频！',
    description: 'Apple watch自带的Safari浏览器最大的痛点是无法播放视频，而我们的浏览器可以。',
    icon: 'i-ph-browser-duotone',
  },
  {
    name: '手表点外卖！',
    description: '我们在背后使用一些特殊的方式使我们可以方便的在手表上直接点外卖！',
    icon: 'i-ph-popcorn-duotone',
  },
]
const musicFeatures = [
  {
    name: '播放音乐！',
    description: '我们的音乐应用可以让你在手表上直接在线播放音乐，并且带有歌词',
    icon: 'i-ph-music-note-duotone',
  },

]
</script>

<template>
  <div id="index" overflow-hidden>
    <GradientBackground>
      <div id="index-heading" class="relative isolate pt-14">
        <div class="py-24 sm:py-32 lg:pb-40">
          <div class="mx-auto max-w-7xl px-6 lg:px-8">
            <div class="mx-auto max-w-2xl text-center">
              <h1 class="text-4xl text-gray-900 font-bold tracking-tight sm:text-6xl dark:text-white">
                Apple watch 腕上系列
              </h1>
              <p class="mt-6 text-lg text-gray-600 leading-8 dark:text-gray-300">
                体验一系列为Apple Watch精心设计的应用，带来便捷与乐趣。<br>探索更多，发现无限可能。
              </p>
            </div>
          </div>
        </div>
        <div class="apple-watch-more absolute right--40 top-0 z--20 bg-no-repeat op-5 dark:op-30 dark:filter-invert-1" />
        <ImageBackground src="/apple-watch-more.svg" right--40 top-0 z--20 />
      </div>

      <div id="index-browser" relative>
        <ImageBackground src="/apple-watch-ultra.svg" bottom--160 left--40 z--20 md:bottom--140 sm:bottom--130 :height="1600" />
        <div class="overflow-hidden py-24 sm:py-32">
          <div class="mx-auto max-w-7xl px-6 lg:px-8">
            <div class="grid grid-cols-1 mx-auto max-w-2xl gap-x-8 gap-y-16 lg:grid-cols-2 lg:mx-0 lg:max-w-none sm:gap-y-20">
              <div class="lg:ml-auto lg:pl-4 lg:pt-4">
                <div class="lg:max-w-lg">
                  <h2 class="text-base text-yellow-600 font-semibold leading-7">
                    闪电工作室
                  </h2>
                  <p class="mt-2 text-3xl text-gray-900 font-bold tracking-tight sm:text-4xl dark:text-white">
                    腕上浏览器
                  </p>
                  <p class="mt-6 text-lg text-gray-600 leading-8 dark:text-gray-300">
                    一款专为Apple Watch设计的全功能浏览器，让你的腕间世界更加丰富多彩。
                  </p>
                  <dl class="mt-10 max-w-xl text-base leading-7 lg:max-w-none space-y-8">
                    <div v-for="feature in browserFeatures" :key="feature.name" class="relative pl-9">
                      <dt class="text-gray-900 font-semibold dark:text-white">
                        <div absolute left-1 top-1 h-5 w-5 text-indigo-500 :class="feature.icon" aria-hidden="true" />
                        {{ feature.name }}
                      </dt>
                      {{ ' ' }}
                      <dd class="inline">
                        {{ feature.description }}
                      </dd>
                    </div>
                  </dl>
                  <div class="ml2 mt10 flex justify-between">
                    <a href="/download" transition-all class="inline-flex items-center justify-center rounded-lg bg-yellow-600 px-6 py-3 text-base text-white font-medium shadow-lg hover:bg-yellow-700">
                      立即下载
                    </a>
                  </div>
                  <div ml2 mt5 inline-block cursor-pointer>
                    <div flex items-center gap1.5 font-size-3.5 transition-all border-b="1 solid yellow-200" hover:border-b="2 solid yellow-300">
                      <div i-carbon-link />
                      <div>如果下载按钮不可用，请点此联系客服</div>
                    </div>
                  </div>
                  <div ml2 mt2 flex flex-wrap gap-x3 font-size-3 op-30>
                    <span>开发者：闪电狮</span>
                    <span>版本号：0.0.0</span>
                    <span>发布时间：{{ new Date().toLocaleDateString() }}</span>
                    <span cursor-pointer border-b="1 solid red-200" hover:border-b="2 solid yellow-300">应用权限</span>
                    <span cursor-pointer border-b="1 solid red-200" hover:border-b="2 solid yellow-300">隐私政策</span>
                  </div>
                </div>
              </div>
              <div class="flex items-start justify-end lg:order-first">
                <img src="../assets/browser-logo.jpeg" class="z-9 w-48rem rounded-xl shadow-xl ring-5 ring-gray-400/10 sm:w-57rem">
              </div>
            </div>
          </div>
        </div>
      </div>

      <div id="index-music">
        <div class="overflow-hidden py-24 sm:py-32">
          <div class="mx-auto max-w-7xl lg:px-8 md:px-6">
            <div class="grid grid-cols-1 gap-x-8 gap-y-16 lg:grid-cols-2 lg:items-start sm:gap-y-20">
              <div class="px-6 lg:px-0 lg:pr-4 lg:pt-4">
                <div class="mx-auto max-w-2xl lg:mx-0 lg:max-w-lg">
                  <h2 class="text-base text-yellow-600 font-semibold leading-7">
                    闪电工作室
                  </h2>
                  <p class="mt-2 text-3xl text-gray-900 font-bold tracking-tight sm:text-4xl dark:text-white">
                    悦音音乐
                  </p>
                  <p class="mt-6 text-lg text-gray-600 leading-8">
                    我们的音乐应用程序可让您直接在手表上播放在线音乐，歌词、收藏、播放列表等功能一应俱全。
                  </p>
                  <dl class="mt-10 max-w-xl text-base text-gray-600 leading-7 lg:max-w-none space-y-8 dark:text-gray-300">
                    <div v-for="feature in musicFeatures" :key="feature.name" class="relative pl-9">
                      <dt class="inline text-gray-900 font-semibold dark:text-white">
                        <div absolute left-1 top-1 h-5 w-5 text-indigo-500 :class="feature.icon" aria-hidden="true" />
                        {{ feature.name }}
                      </dt>
                      {{ ' ' }}
                      <dd class="inline">
                        {{ feature.description }}
                      </dd>
                    </div>
                    <div ml2 mt10 flex justify-between>
                      <a href="/download" transition-all class="inline-flex items-center justify-center rounded-lg bg-red-600 px-6 py-3 text-base text-white font-medium shadow-lg hover:bg-yellow-700">
                        立即下载
                      </a>
                    </div>
                    <div ml2 mt5 inline-block cursor-pointer>
                      <div flex items-center gap1.5 font-size-3.5 transition-all border-b="1 solid yellow-200" hover:border-b="2 solid yellow-300">
                        <div i-carbon-link />
                        <div>如果下载按钮不可用，请点此联系客服</div>
                      </div>
                    </div>
                    <div ml2 flex flex-wrap gap-x3 font-size-3 op-30>
                      <span>开发者：闪电狮</span>
                      <span>版本号：0.0.0</span>
                      <span>发布时间：{{ new Date().toLocaleDateString() }}</span>
                      <span cursor-pointer border-b="1 solid red-200" hover:border-b="2 solid yellow-300">应用权限</span>
                      <span cursor-pointer border-b="1 solid red-200" hover:border-b="2 solid yellow-300">隐私政策</span>
                    </div>
                  </dl>
                </div>
              </div>
              <div class="lg:px-0 sm:px-6">
                <div class="relative isolate overflow-hidden bg-indigo-500 px-6 pt-8 lg:mx-0 sm:mx-auto lg:max-w-none sm:max-w-2xl sm:rounded-3xl sm:pl-16 sm:pr-0 sm:pt-16">
                  <div class="absolute w-full origin-bottom-left skew-x-[-30deg] bg-indigo-100 opacity-20 ring-1 ring-white ring-inset -inset-y-px -left-3 -z-10" aria-hidden="true" />
                  <div class="mx-auto max-w-2xl sm:mx-0 sm:max-w-none">
                    <img src="https://tailwindui.starxg.com/img/component-images/project-app-screenshot.png" alt="Product screenshot" width="2432" height="1442" class="max-w-none w-[57rem] rounded-tl-xl bg-gray-800 ring-1 ring-white/10 -mb-12">
                  </div>
                  <div class="pointer-events-none absolute inset-0 ring-1 ring-black/10 ring-inset sm:rounded-3xl" aria-hidden="true" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div id="index-about-out-old-apps" relative mx-auto max-w-7xl px-6 lg:px-8>
        <h1 font-size-8 font-bold md:font-size-15>
          关于我们的旧APP...
        </h1>
        <p mt2 font-size-3.5 text-gray-600 sm:mt1 sm:font-size-4 dark:text-gray-300>
          我们之前开发过一些应用，但是由于种种原因，我们现在已经下架了这些应用。如果您曾在我们的应用上消费过，点击下方的退款按钮，我们会尽快为您处理。
        </p>
      </div>
    </GradientBackground>
  </div>
</template>
