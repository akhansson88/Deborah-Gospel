<template>
  <div class="container mx-auto p-6">
    <h3 class="text-xl text-debby-dark font-bold mb-4">Music Showcase</h3>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
      <div v-for="track in tracks" :key="track.id" class="bg-white shadow-lg rounded-lg p-4">
        <div class="flex flex-col items-center">
          <img :src="track.cover" alt="Album Cover" class="w-full rounded-md mb-4">
          <h4 class="text-md font-semibold">{{ track.title }}</h4>
          <p class="text-sm text-gray-600">{{ track.album }}</p>
          <!-- Additional track details -->
          <audio controls>
            <source :src="track.sample" type="audio/mpeg">
            Your browser does not support the audio element.
          </audio>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Mock data, should be fetched from an API or store
      tracks: [
        {
          id: 1,
          title: 'My Lord Exists',
          album: 'The Journey',
          cover: require('~/assets/img/mylordexists_album.jpg'),
          sample: '~/assets/music/sample_1.mp3'
        },
        // ... more tracks
      ]
    }
  }
}
</script>

<style>
/* Custom styles if needed */
</style>
