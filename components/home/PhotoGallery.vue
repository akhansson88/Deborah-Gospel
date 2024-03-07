<template>
  <div class="container mx-auto p-6">
    <h3 class="text-xl text-debby-dark font-bold mb-4">Photo Gallery</h3>
    <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
      <div v-for="image in images" :key="image.id" class="overflow-hidden rounded-lg shadow-lg">
        <img :src="image.src" :alt="image.alt" class="w-full h-full object-cover object-center transition-transform duration-300 hover:scale-110">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Mock data, should ideally be fetched from an API or store
      images: [
        { id: 1, src: '~/assets/img/gallery/image1.jpg', alt: 'Description of image 1' },
        { id: 2, src: '~/assets/img/gallery/image2.jpg', alt: 'Description of image 2' },
        // ... more images
      ]
    }
  }
}
</script>

<style>
/* Custom styles if needed */
</style>
