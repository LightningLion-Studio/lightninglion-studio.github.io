<script setup lang="tsx">
type Features = {
  name: string
  description: string
  icon: string
}[]

defineProps({
  name: String,
  title: String,
  desc: String,
  features: {
    type: Array as PropType<Features>,
    default: [] as Features,
  },
  src: String,
})

const emit = defineEmits(['contact-click', 'download-click'])
</script>

<template>
  <section class="overflow-hidden py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl flex flex-col gap-x-8 gap-y-16 lg:grid-cols-2 lg:mx-0 lg:max-w-none md:flex-row sm:gap-y-20">
        <div class="lg:pl-4 lg:pt-4">
          <div class="lg:max-w-xl">
            <h2 class="text-base text-yellow-600 font-semibold leading-7">
              {{ name }}
            </h2>
            <p class="mt-2 text-3xl text-gray-900 font-bold tracking-tight sm:text-4xl dark:text-white">
              {{ title }}
            </p>
            <p class="mt-6 text-lg text-gray-600 leading-8 dark:text-gray-300">
              {{ desc }}
            </p>
            <dl class="mt-10 max-w-xl text-base leading-7 lg:max-w-none space-y-8">
              <div v-for="feature in features" :key="feature.name" class="relative pl-9">
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
              <button transition-all class="inline-flex items-center justify-center rounded-lg bg-yellow-600 px-6 py-3 text-base text-white font-medium shadow-lg hover:bg-yellow-700" @click="emit('download-click')">
                立即下载
              </button>
            </div>
            <div ml2 mt5 inline-block cursor-pointer>
              <div flex items-center gap1.5 font-size-3.5 transition-all border-b="1 solid yellow-200" hover:border-b="2 solid yellow-300" @click="emit('contact-click')">
                <div i-carbon-link />
                <div>如果下载按钮不可用，请点此联系客服</div>
              </div>
            </div>
            <slot name="footer" />
          </div>
        </div>
        <div class="flex items-start justify-end lg:order-first">
          <img :src="src" class="z-9 w-48rem rounded-xl shadow-xl ring-5 ring-gray-400/10 md:w-30rem">
        </div>
      </div>
    </div>
  </section>
</template>
