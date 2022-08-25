<template>
  <section class="home-page flex column main-layout">
    <hero></hero>
  </section>
</template>

<script>
import Hero from '../cmps/Hero.vue'
export default {
  components: { Hero },
  data() {
    return {
      articles: null,
    }
  },
}
</script>
