<template>
  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
    <div v-for="course in courses" :key="course.id" class="rounded overflow-hidden shadow-lg p-4 bg-white">
      <img class="w-full" :src="course.image" :alt="course.title">
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">{{ course.title }}</div>
        <p class="text-gray-700 text-base">
          {{ course.description }}
        </p>
      </div>
      <div class="px-6 pt-4 pb-2">
        <span class="inline-block bg-debby-skyblue rounded-full px-3 py-1 text-sm font-semibold text-white mr-2 mb-2">More Info</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      courses: [
        {
          id: 1,
          title: 'Basics of Gospel Singing',
          description: 'Learn the foundational techniques of gospel singing.',
          image: require('@/assets/img/teaching_music.jpg')
        },
        // Add more courses as needed
      ]
    }
  }
}
</script>
