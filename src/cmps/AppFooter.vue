<template>
  <footer class="app-footer flex space-between">
    <div class="resources flex">
      <div v-for="resource in footerLinks" class="resource" :key="resource">
        <h3 class="bold">{{ resource.title }}</h3>
        <ul class="link-list clean-list flex column">
          <li v-for="link in resource.links" :key="link">
            {{ link }}
          </li>
        </ul>
      </div>
    </div>
    <div class="logo">
      <img src="@/assets/imgs/footer-logo.png" alt="" />
    </div>
  </footer>
</template>

<script>
export default {
  computed: {
    footerLinks() {
      return [
        {
          title: 'בלימודים',
          links: ['מאגר מורים פרטיים', 'ארכיוני מבחנים', 'אזור מרתונים'],
        },
        {
          title: 'בקמפוס',
          links: ['מאגר מורים פרטיים', 'ארכיוני מבחנים', 'אזור מרתונים'],
        },
        {
          title: 'באגודה',
          links: ['מאגר מורים פרטיים', 'ארכיוני מבחנים', 'אזור מרתונים'],
        },
        {
          title: 'אזור אישי',
          links: ['מאגר מורים פרטיים', 'ארכיוני מבחנים', 'אזור מרתונים'],
        },
        {
          title: 'כללי',
          links: ['מאגר מורים פרטיים', 'ארכיוני מבחנים', 'אזור מרתונים'],
        },
      ]
    },
  },
}
</script>

<style></style>
