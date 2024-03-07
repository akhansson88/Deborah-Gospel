<template>
  <section class="py-8 bg-debby-white">
    <div class="container mx-auto px-6">
      <h3 class="text-2xl font-semibold text-debby-dark mb-4">Upcoming Events</h3>
      <div class="space-y-6">
        <div 
          v-for="event in events" 
          :key="event.id" 
          class="border p-4 rounded-lg shadow-sm hover:shadow-md transition-shadow"
        >
          <h4 class="font-bold text-lg">{{ event.title }}</h4>
          <p class="text-sm text-gray-600">{{ event.date | formatDate }}</p>
          <p>{{ event.summary }}</p>
          <nuxt-link 
            :to="`/events/${event.id}`"
            class="text-debby-skyblue hover:text-debby-dark transition-colors"
          >
            Learn More
          </nuxt-link>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      // This will be replaced with actual data fetching from an API or static file
      events: [
        { id: 1, title: 'Worship Night in Kigali', date: new Date('2024-05-20'), summary: 'Join Deborah for a night of worship and praise.' },
        // ... more events
      ]
    }
  },
  filters: {
    formatDate(value) {
      // A simple filter to format date, consider using a library like date-fns or moment.js for more complex needs
      if (value) {
        return new Intl.DateTimeFormat('en-US', { month: 'long', day: 'numeric', year: 'numeric' }).format(new Date(value));
      }
    }
  }
}
</script>

<style>
/* Custom styles if needed */
</style>
