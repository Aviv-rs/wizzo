<template>
  <section className="job-list">
    <header class="flex space-between">
      <h2 class="bold">לוח משרות</h2>
    </header>
    <div class="list-container">
      <div v-for="(job, idx) in jobs" :key="idx">
        <JobPreview :job="job" />
      </div>
    </div>
  </section>
</template>

<script>
import JobPreview from './JobPreview.vue'
export default {
  props: {
    jobs: {
      required: true,
      type: Array,
    },
  },
  components: {
    JobPreview,
  },
}
</script>

<style></style>
