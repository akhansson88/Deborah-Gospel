<template>
  <div class="min-h-screen bg-white py-10">
    <div class="container mx-auto px-4">
      <h1 class="text-4xl font-bold text-center text-debby-dark mb-12">Gallery</h1>
      <!-- Photo Gallery Component -->
      <PhotoGallery />
    </div>
  </div>
</template>

<script>
import PhotoGallery from '~/components/home/PhotoGallery.vue';

export default {
  components: {
    PhotoGallery
  },
  head() {
    return {
      title: 'Gallery - Deborah Uwitonze',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Explore the gallery to see photos of Deborah Uwitonze, including events, behind-the-scenes, and more.'
        }
      ]
    }
  }
}
</script>

<style>
/* Additional styling specific to the gallery page */
</style>
