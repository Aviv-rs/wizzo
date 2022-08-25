<template>
  <AppHeader />
  <main class="route">
    <RouterView />
  </main>
  <AppFooter></AppFooter>
</template>

<script>
import '@/assets/styles/main.scss'
import AppHeader from '@/cmps/AppHeader.vue'
import AppFooter from './cmps/AppFooter.vue'

export default {
  components: {
    AppHeader,
    AppFooter,
  },
}
</script>
