<template>
  <section class="press-feature py-12 bg-white">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-center text-debby-dark mb-8">In the Press</h2>
      <div class="flex flex-wrap justify-center items-center gap-8">
        <div v-for="feature in pressFeatures" :key="feature.id" class="max-w-sm">
          <a :href="feature.link" target="_blank" rel="noopener noreferrer">
            <img :src="feature.image" :alt="feature.title" class="mb-4 rounded shadow-lg">
            <h3 class="text-xl font-semibold mb-2">{{ feature.title }}</h3>
          </a>
          <p class="text-gray-600 text-sm">{{ feature.excerpt }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      pressFeatures: [
        {
          id: 1,
          title: 'Deborah Uwitonze: The Voice of Modern Gospel',
          excerpt: 'An in-depth look at Deborah\'s journey in the gospel music scene.',
          image: 'https://images.unsplash.com/photo-1503694978374-8a2fa686963a?q=80&w=2069&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
          link: 'https://example.com/article1'
        },
        // More press features here
      ]
    }
  }
}
</script>

<style>
/* Styling for the PressFeature component */
</style>
