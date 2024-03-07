<template>
  <section class="latest-music py-12 bg-gray-50">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-center text-debby-dark mb-8">Latest Music</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8">
        <div v-for="track in latestTracks" :key="track.id" class="rounded overflow-hidden shadow-lg bg-white">
          <img :src="track.cover" alt="Album cover" class="w-full">
          <div class="px-6 py-4">
            <div class="font-bold text-xl mb-2">{{ track.title }}</div>
            <p class="text-gray-700 text-base">{{ track.description }}</p>
          </div>
          <div class="px-6 pt-4 pb-2">
            <NuxtLink :to="track.link">
              <button class="bg-debby-skyblue hover:bg-debby-dark text-white font-bold py-2 px-4 rounded">
                Listen
              </button>
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      // Sample data structure. Replace with your actual data source
      latestTracks: [
        {
          id: 1,
          title: 'Heavenly Voice',
          description: 'A soul-touching melody that uplifts the spirit.',
          cover: require('@/assets/img/Izina_Rya_Yesu_AlbumCover.jpg'),
          link: '/music#heavenly-voice' // Link to detailed page or external streaming platform
        },
        // Additional tracks as per your latest releases
      ]
    }
  }
}
</script>

<style>
/* Styling specific to LatestMusic component */
</style>
