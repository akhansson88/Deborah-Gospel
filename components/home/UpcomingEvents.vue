<template>
  <section class="upcoming-events py-12">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-center text-debby-dark mb-8">Upcoming Events</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="event in events" :key="event.id" class="rounded overflow-hidden shadow-lg bg-white">
          <img :src="event.image" alt="Event image" class="w-full">
          <div class="px-6 py-4">
            <div class="font-bold text-xl mb-2">{{ event.name }}</div>
            <p class="text-gray-700 text-base mb-4">{{ event.date | formatDate }}</p>
            <p class="text-gray-700 text-base">{{ event.location }}</p>
          </div>
          <div class="px-6 pt-4 pb-2">
            <NuxtLink :to="event.link">
              <button class="bg-debby-skyblue hover:bg-debby-dark text-white font-bold py-2 px-4 rounded">
                More Info
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
      events: [
        {
          id: 1,
          name: 'Gospel Night in Kigali',
          date: new Date('2024-04-30'),
          location: 'Kigali, Rwanda',
          image: 'https://images.unsplash.com/photo-1503694978374-8a2fa686963a?q=80&w=2069&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
          link: '/events#gospel-night' // This can be a link to a detailed page or external ticketing service
        },
        // More events here
      ]
    }
  },
  filters: {
    formatDate(value) {
      if (value) {
        const options = { year: 'numeric', month: 'long', day: 'numeric' };
        return value.toLocaleDateString('en-US', options);
      }
      return '';
    }
  }
}
</script>

<style>
/* Styling specific to UpcomingEvents component */
</style>
