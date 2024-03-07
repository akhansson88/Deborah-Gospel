<template>
  <div>
    <HeroSection />
    <AboutSection />
    <LatestMusic />
    <UpcomingEvents />
    <MusicVideoSpotlight />
    <NewsletterSignup />
    <PressFeature />
  </div>
</template>

<script>
import HeroSection from '~/components/home/HeroSection.vue'
import AboutSection from '~/components/home/AboutSection.vue'
import LatestMusic from '~/components/home/LatestMusic.vue'
import UpcomingEvents from '~/components/home/UpcomingEvents.vue'
import MusicVideoSpotlight from '~/components/home/MusicVideoSpotlight.vue'
import NewsletterSignup from '~/components/common/NewsletterSignup.vue'
import PressFeature from '~/components/home/PressFeature.vue'
  
export default {
  name: 'IndexPage',
  components: {
    HeroSection,
    AboutSection,
    LatestMusic,
    UpcomingEvents,
    MusicVideoSpotlight,
    NewsletterSignup,
    PressFeature
  }
}
</script>
