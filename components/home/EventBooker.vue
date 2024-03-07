<template>
  <div class="container mx-auto p-6">
    <h3 class="text-xl text-debby-dark font-bold mb-4">Book Deborah for Your Event</h3>
    <form @submit.prevent="submitBooking" class="bg-white shadow-lg rounded-lg p-4">
      <div class="grid grid-cols-1 gap-4 mb-4">
        <!-- Form fields go here -->
        <input type="text" placeholder="Your Name" class="border p-2 rounded" required>
        <input type="email" placeholder="Your Email" class="border p-2 rounded" required>
        <textarea placeholder="Event Details" class="border p-2 rounded" required></textarea>
      </div>
      <button type="submit" class="bg-debby-skyblue text-white p-2 rounded">Submit Booking Request</button>
    </form>
  </div>
</template>

<script>
export default {
  methods: {
    submitBooking() {
      // Handle the booking submission
      alert('Booking request submitted!');
      // Here, you would typically send the data to a backend service
    }
  }
}
</script>
