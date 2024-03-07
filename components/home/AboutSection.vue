<template>
  <section class="about-section py-12">
    <div class="container mx-auto px-6">
      <div class="flex flex-wrap items-center">
        <div class="w-full md:w-1/2">
          <img src="https://images.unsplash.com/photo-1545315003-c5ad6226c272?q=80&w=1064&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Deborah Uwitonze" class="rounded shadow-lg">
        </div>
        <div class="w-full md:w-1/2 md:pl-10">
          <h2 class="text-3xl font-bold text-debby-dark mb-4">About Deborah</h2>
          <p class="text-lg text-gray-700 mb-4">
            Deborah Uwitonze, born and raised in Kigali, Rwanda, discovered her passion for gospel music at a young age. Called to share her faith through song, Deborah has touched the hearts of many across the globe.
          </p>
          <p class="text-lg text-gray-700 mb-4">
            Her music, a blend of traditional gospel rhythms and contemporary sounds, seeks to inspire and uplift her listeners. Through her melodies, Deborah tells stories of faith, hope, and love.
          </p>
          <NuxtLink to="/bio">
            <button class="bg-debby-skyblue hover:bg-debby-dark text-white font-bold py-2 px-4 rounded">
              Learn More
            </button>
          </NuxtLink>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
}
</script>

<style>
/* Optional: Add styles specific to the AboutSection here */
</style>
