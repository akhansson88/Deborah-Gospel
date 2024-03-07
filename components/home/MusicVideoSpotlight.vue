<template>
  <section class="music-video-spotlight py-12 bg-gray-100">
    <div class="container mx-auto px-6 text-center">
      <h2 class="text-3xl font-bold text-debby-dark mb-8">Featured Music Video</h2>
      <div class="relative h-0" style="padding-bottom: 56.25%"> <!-- 16:9 Aspect Ratio -->
        <iframe class="absolute top-0 left-0 w-full h-full" :src="videoUrl" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
      <div class="mt-8">
        <h3 class="text-xl font-semibold">{{ title }}</h3>
        <p class="mt-4 text-gray-600">{{ description }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      title: 'IZINA RYA YESU',
      description: 'A soul-stirring music video that captures the essence of Deborah\'s faith and vocal power. Filmed in the scenic landscapes of Rwanda, this video brings to life the heartfelt worship of her gospel music.',
      videoUrl: 'https://www.youtube.com/embed/BQV5EbPGnCs' // Replace with your actual YouTube embed link
    }
  }
}
</script>

<style>
/* You can add custom styles for your MusicVideoSpotlight component here */
.music-video-spotlight iframe {
  /* Ensures the iframe is responsive */
}
</style>
