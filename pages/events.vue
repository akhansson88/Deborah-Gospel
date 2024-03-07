<template>
  <section class="py-8 bg-white">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-semibold text-debby-dark mb-6">Upcoming Events</h2>
      <!-- EventCalendar component to display events in a calendar view -->
      <EventCalendar :events="events" />
      <!-- Additional event details or links to individual event pages could go here -->
      <div v-for="event in events" :key="event.id" class="mt-6">
        <div class="max-w-4xl mx-auto bg-debby-light p-4 rounded-lg shadow">
          <h3 class="font-semibold text-xl">{{ event.title }}</h3>
          <p class="text-md">{{ event.date | formatDate }}</p>
          <p class="mt-2">{{ event.description }}</p>
          <nuxt-link :to="`/events/${event.id}`" class="text-debby-skyblue mt-4 inline-block">Read more &rarr;</nuxt-link>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import EventCalendar from '~/components/events/EventCalendar.vue'

export default {
  components: {
    EventCalendar
  },
  data() {
    return {
      // Mock data for the purpose of this example, replace with dynamic data from your backend or API
      events: [
        { id: 1, title: 'Gospel Concert', date: '2024-04-15', description: 'Join Deborah for a night of worship and gospel music.' },
        { id: 2, title: 'Charity Event Performance', date: '2024-05-20', description: 'Support a good cause with Deborah at the charity event.' },
        // More events here
      ]
    }
  },
  filters: {
    formatDate(value) {
      if (value) {
        return new Date(value).toLocaleDateString('en-US', {
          year: 'numeric', month: 'long', day: 'numeric'
        });
      }
    }
  }
}
</script>
