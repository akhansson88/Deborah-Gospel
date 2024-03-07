<template>
  <section class="newsletter-signup py-12 bg-debby-skyblue text-white">
    <div class="container mx-auto px-6 text-center">
      <h2 class="text-3xl font-bold mb-4">Stay Updated</h2>
      <p class="mb-8">Subscribe to our newsletter for the latest on new music, events, and more.</p>
      <form @submit.prevent="submitForm" class="flex justify-center items-center gap-4">
        <input type="email" v-model="email" placeholder="Enter your email" required class="p-2 rounded w-full max-w-md">
        <button type="submit" class="bg-debby-dark hover:bg-debby-maroon font-bold py-2 px-4 rounded">
          Subscribe
        </button>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      email: '',
    }
  },
  methods: {
    submitForm() {
      // Implement subscription logic here. Could be an API call to a newsletter service.
      console.log('Subscribing with email:', this.email);
      alert('Thank you for subscribing!');
      this.email = ''; // Reset the input field after submission
    }
  }
}
</script>

<style>
/* Additional styling for the NewsletterSignup component */
</style>
