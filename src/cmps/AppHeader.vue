<template>
  <header class="app-header">
    <nav class="links flex">
      <RouterLink v-for="link in links" :key="link" to="/">{{
        link
      }}</RouterLink>
    </nav>
  </header>
</template>

<script>
export default {
  computed: {
    links: () => [
      'אקדמי',
      'רווחה',
      'דוברות',
      'לוח אירועים',
      'על האגודה',
      'לוח משרות',
      'הטבות לחברי האגודה',
      'דברו איתנו',
    ],
  },
}
</script>
