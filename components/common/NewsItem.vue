<template>
  <div class="max-w-md w-full lg:flex mb-4 shadow-lg">
    <div class="h-48 lg:h-auto lg:w-48 flex-none bg-cover rounded-t lg:rounded-t-none lg:rounded-l text-center overflow-hidden" :style="{ backgroundImage: 'url(' + news.image + ')' }" title="News image"></div>
    <div class="border-r border-b border-l border-gray-200 lg:border-l-0 lg:border-t lg:border-gray-200 bg-white rounded-b lg:rounded-b-none lg:rounded-r p-4 flex flex-col justify-between leading-normal">
      <div class="mb-8">
        <div class="text-gray-900 font-bold text-xl mb-2">{{ news.title }}</div>
        <p class="text-gray-700 text-base">{{ news.summary }}</p>
      </div>
      <div class="flex items-center">
        <div class="text-sm">
          <p class="text-gray-600">Published on {{ news.date }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    news: {
      type: Object,
      required: true
    }
  }
}
</script>
