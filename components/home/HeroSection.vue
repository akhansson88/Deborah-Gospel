<template>
  <div class="hero-section bg-cover bg-center" :style="{ backgroundImage: 'url(' + backgroundImage + ')' }">
    <div class="text-center text-white p-12">
      <h1 class="text-5xl font-bold mb-4">Deborah Uwitonze</h1>
      <p class="text-xl mb-8">Spreading the Gospel Through Melody</p>
      <NuxtLink to="/music">
        <button class="bg-debby-skyblue hover:bg-debby-dark text-white font-bold py-2 px-4 rounded">
          Explore Music
        </button>
      </NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      backgroundImage: 'https://images.unsplash.com/photo-1526746323784-6bc814d79273?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' // Update this path with your image
    }
  }
}
</script>

<style>
.hero-section {
  height: 75vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background-size: cover;
}
</style>
