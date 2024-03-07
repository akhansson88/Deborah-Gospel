<template>
  <div class="min-h-screen bg-white py-10">
    <div class="container mx-auto px-4">
      <h1 class="text-4xl font-bold text-center text-debby-dark mb-12">Music</h1>
      <!-- Music Showcase Component -->
      <MusicShowcase />
    </div>
  </div>
</template>

<script>
import MusicShowcase from '~/components/home/MusicShowcase.vue';

export default {
  components: {
    MusicShowcase
  },
  head() {
    return {
      title: 'Music - Deborah Uwitonze',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Explore the music of Deborah Uwitonze, including albums, singles, and music videos.'
        }
      ]
    }
  }
}
</script>

<style>
/* Additional styling specific to the music page */
</style>
