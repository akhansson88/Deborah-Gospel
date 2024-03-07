<template>
  <section class="py-8">
    <div class="container mx-auto px-6">
      <div class="w-full lg:w-4/5 mx-auto mb-12">
        <h2 class="text-3xl font-semibold text-debby-dark mb-6">About Deborah</h2>
        <img 
          src="~/assets/img/deborah_uwitonze_profile.jpeg" 
          alt="Deborah Uwitonze" 
          class="rounded-full mb-6 w-64 h-64 object-cover mx-auto"
        >
        <div class="text-lg text-gray-700 space-y-4">
          <p>
            Deborah Uwitonze is a renowned gospel singer from Kigali, Rwanda, with a passion for spreading the message of faith through her music. She began singing as a child and has always felt a divine calling to sing for God.
          </p>
          <p>
            Over the years, Deborah has inspired many with her powerful voice and heartfelt lyrics. Her music resonates with people across the world, bringing hope and comfort to those who listen.
          </p>
          <!-- More paragraphs about her biography -->
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  head() {
    return {
      title: 'Biography - Deborah Uwitonze',
      meta: [
        // Meta tags for SEO
        {
          hid: 'description',
          name: 'description',
          content: 'Learn about Deborah Uwitonze, a gospel singer from Kigali, Rwanda, and her musical journey.'
        }
      ]
    }
  }
}
</script>

<style>
/* Custom styles if needed */
</style>
