<script setup lang="tsx">
import b from '../assets/腕上B站.png'
import music from '../assets/腕上音乐.png'
import novel from '../assets/腕上小说.png'
import assistant from '../assets/腕上小助手.png'
import news from '../assets/腕上资讯.png'
import cherry from '../assets/腕上樱花.png'
import browser from '../assets/browser-logo.jpeg'
import musicV2 from '../assets/悦音音乐.png'
import meow from '../assets/喵哩喵哩.png'

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
const meowFeatures = [
  {
    name: '登录、动态、评论',
    description: '支持登录、查看动态、评论等功能，一个不差。',
    icon: 'i-ph-user-duotone',
  },
  {
    name: '弹幕、点赞、收藏、关注',
    description: '支持弹幕、点赞、收藏、关注等功能，让您的体验更加丰富。',
    icon: 'i-ph-chat-duotone',
  },
  {
    name: '搜索、排行榜、频道',
    description: '支持搜索、查看排行榜、查看频道等功能，B站的核心功能都有。',
    icon: 'i-ph-ranking-duotone',
  },
  {
    name: '历史记录、播放记录',
    description: '支持查看历史记录、播放记录等功能，让您的体验更加便捷。',
    icon: 'i-ph-log-duotone',
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
        <FeatureSection
          name="闪电工作室"
          title="腕上浏览器"
          desc="一款专为Apple Watch设计的全功能浏览器，让你的腕间世界更加丰富多彩。"
          :features="browserFeatures"
          :src="browser"
        >
          <template #footer>
            <AppInfoFooter developer="闪电狮" version="0.0.0" />
          </template>
        </FeatureSection>
      </div>

      <div id="index-music" relative>
        <FeatureSection
          name="闪电工作室"
          title="悦音音乐"
          desc="我们的音乐应用程序可让您直接在手表上播放在线音乐，歌词、收藏、播放列表等功能一应俱全。"
          :features="musicFeatures"
          :src="musicV2"
        >
          <template #footer>
            <AppInfoFooter developer="闪电狮" version="0.0.0" />
          </template>
        </FeatureSection>
      </div>

      <div id="index-about-out-old-apps" relative mx-auto max-w-7xl px-6 lg:px-8>
        <div class="py-24 sm:py-32">
          <div class="grid grid-cols-1 items-center gap-x-8 gap-y-16 lg:grid-cols-2">
            <div class="mx-auto max-w-xl w-full lg:mx-0">
              <h2 class="text-3xl text-gray-900 font-bold tracking-tight dark:text-white">
                关于我们的旧APP...
              </h2>
              <p class="mt-6 text-lg text-gray-600 leading-8 dark:text-white">
                我们之前开发过一些应用，但是由于种种原因，我们现在已经下架了这些应用。如果您曾在我们的应用上消费过，点击下方的退款按钮，我们会尽快为您处理。
              </p>
              <div class="mt-8 flex items-center gap-x-6">
                <a href="#" class="rounded-md bg-indigo-600 px-7.5 py-3.5 text-sm text-size-4.5 text-white font-semibold shadow-sm hover:bg-indigo-500 focus-visible:outline-2 focus-visible:outline-indigo-600 focus-visible:outline-offset-2 focus-visible:outline">退款</a>
                <!-- <a href="#" class="text-sm text-gray-900 font-semibold">退款<span aria-hidden="true">&rarr;</span></a> -->
              </div>
            </div>
            <div class="grid grid-cols-2 mx-auto max-w-xl w-full items-center gap-y-12 lg:mx-0 lg:max-w-none sm:gap-y-14 lg:pl-8">
              <BrandItem :src="b" name="腕上B站" />
              <BrandItem :src="music" name="腕上音乐" />
              <BrandItem :src="novel" name="腕上小说" />
              <BrandItem :src="assistant" name="腕上小助手" />
              <BrandItem :src="news" name="腕上资讯" />
              <BrandItem :src="cherry" name="腕上樱花" />
            </div>
          </div>
        </div>
      </div>

      <div id="index-about-meow" relative mx-auto max-w-7xl px-6 lg:px-8>
        <div class="flex flex-col items-center gap-5 pt24 sm:pt32">
          <img block w-7em rounded-full :src="meow">
          <h1 text-center font-size-10 font-bold>
            腕上B站的替代品：喵哩喵哩
          </h1>
          <p max-w-4xl text-center>
            由Darock Studio出品的喵哩喵哩拥有极致的性能和优秀的设计，完全可以替代腕上B站，以让您更好地浏览专属于您的视频信息流，现功能基本与腕上B站相当。
          </p>
        </div>
        <div class="mx-auto mt12 max-w-2xl lg:mt-24 lg:max-w-4xl">
          <dl class="grid grid-cols-1 max-w-xl gap-x-8 gap-y-10 lg:grid-cols-2 lg:max-w-none lg:gap-y-16">
            <div v-for="feature in meowFeatures" :key="feature.name" class="relative pl-16">
              <dt class="text-base text-gray-900 font-semibold leading-7 dark:text-white">
                <div class="absolute left-0 top-0 h-10 w-10 flex items-center justify-center rounded-lg bg-pink-600">
                  <div :class="feature.icon" class="h-6 w-6 text-white" aria-hidden="true" />
                </div>
                {{ feature.name }}
              </dt>
              <dd class="mt-2 text-base text-gray-600 leading-7 dark:text-gray-400">
                {{ feature.description }}
              </dd>
            </div>
          </dl>
        </div>
        <div mb24 mt12 flex justify-center sm:mt24>
          <button class="rounded-md bg-pink-600 px-7.5 py-3.5 text-sm text-size-4.5 text-white font-semibold shadow-sm hover:bg-pink-500 focus-visible:outline-2 focus-visible:outline-pink-600 focus-visible:outline-offset-2 focus-visible:outline">
            立即下载
          </button>
        </div>
      </div>
    </GradientBackground>
  </div>
</template>
