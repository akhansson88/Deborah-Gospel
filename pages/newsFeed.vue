<template>
  <div class="container mx-auto">
    <h1 class="text-2xl font-bold my-4">Latest News</h1>
    <div class="space-y-4">
      <NewsItem 
        v-for="item in newsItems" 
        :key="item.id" 
        :news="item" 
      />
    </div>
  </div>
</template>

<script>
import NewsItem from '~/components/common/NewsItem.vue'

export default {
  components: {
    NewsItem
  },
  data() {
    return {
      newsItems: [
        {
          id: 1,
          title: 'New Album Release',
          summary: 'Deborah Uwitonze releases her new gospel album, featuring inspirational songs.',
          date: '2024-03-01',
          image: 'path/to/image.jpg'
        },
        // More news items
      ]
    }
  }
}
</script>
