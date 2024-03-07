<template>
  <nav class="bg-debby-dark text-debby-white p-4">
    <div class="container mx-auto flex justify-between items-center">
      <h1 class="text-xl font-bold">Deborah Uwitonze</h1>
      <ul class="flex space-x-4">
        <li><NuxtLink to="/">Home</NuxtLink></li>
        <li><NuxtLink to="/bio">Biography</NuxtLink></li>
        <li><NuxtLink to="/events">Events</NuxtLink></li>
        <li><NuxtLink to="/music">Music</NuxtLink></li>
        <li><NuxtLink to="/gallery">Gallery</NuxtLink></li>
        <li><NuxtLink to="/courses">Courses</NuxtLink></li>
        <li><NuxtLink to="/shop">Shop</NuxtLink></li>
        <li><NuxtLink to="/newsFeed">News Feed</NuxtLink></li>
        <!-- Additional links can be added here -->
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  // Component details
}
</script>

<style>
/* Style adjustments if necessary */
</style>
