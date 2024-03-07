<template>
  <div class="container mx-auto p-6">
    <h3 class="text-xl text-debby-dark font-bold mb-4">Upcoming Events</h3>
    <div class="bg-white shadow-lg rounded-lg p-4">
      <ul class="divide-y-2 divide-gray-100">
        <li v-for="event in events" :key="event.id" class="py-4">
          <div class="flex justify-between items-center">
            <div>
              <h4 class="text-debby-dark font-semibold">{{ event.title }}</h4>
              <p class="text-sm text-gray-600">{{ event.date | formatDate }}</p>
            </div>
            <a href="#" class="text-debby-skyblue">Details</a>
          </div>
        </li>
        <!-- More events here -->
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Mock data, should be fetched from an API or store
      events: [
        { id: 1, title: 'Gospel Concert', date: '2024-04-15' },
        { id: 2, title: 'Charity Event Performance', date: '2024-05-20' },
        // ... more events
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
