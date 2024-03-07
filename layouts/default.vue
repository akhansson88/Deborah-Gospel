<template>
  <div>
    <Navigation />
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
import Navigation from '~/components/common/Navigation.vue'
import Footer from '~/components/common/Footer.vue'

export default {
  components: {
    Navigation,
    Footer
  }
}
</script>
