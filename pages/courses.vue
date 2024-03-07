<template>
  <div class="min-h-screen bg-white py-10">
    <div class="container mx-auto px-4">
      <h1 class="text-4xl font-bold text-center text-debby-dark mb-12">Courses</h1>
      <!-- Courses List Component -->
      <CourseList />
    </div>
  </div>
</template>

<script>
import CourseList from '~/components/courses/CourseList.vue';

export default {
  components: {
    CourseList
  },
  head() {
    return {
      title: 'Courses - Deborah Uwitonze',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Learn singing and music from Deborah Uwitonze through our comprehensive courses designed for all levels.'
        }
      ]
    }
  }
}
</script>

<style>
/* Additional styling specific to the courses page */
</style>
