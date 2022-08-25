<template>
  <header class="app-header">
    <div class="logo">
      <img src="@/assets/imgs/header-logo.png" alt="" />
    </div>
    <nav class="links flex">
      <RouterLink class="link" v-for="link in links" :key="link" to="/">{{
        link
      }}</RouterLink>
    </nav>

    <button class="btn-account flex align-center">
      <div class="icon">
        <img src="@/assets/imgs/smiley-icon.png" alt="" />
      </div>
      <span> איזור אישי </span>
    </button>
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
