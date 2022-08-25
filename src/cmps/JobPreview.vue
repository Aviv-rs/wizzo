<template>
  <article className="job-preview flex column">
    <h3 class="bold">{{ job.title }}</h3>
    <p>{{ job.desc }}</p>
    <div class="job-info-container flex">
      <div class="employer flex align-center">
        <div class="img-container">
          <img src="@/assets/imgs/jobs/1.png" alt="" />
        </div>
        <span>
          {{ job.employer }}
        </span>
      </div>
      <div
        v-for="(field, idx) in jobSubfields"
        :key="field[0]"
        class="subfield flex align-center"
      >
        <div class="img-container">
          <img :src="getImgUrl(`../assets/imgs/jobs/${idx + 2}.svg`)" alt="" />
        </div>
        <span> {{ getTranslation(field[0]) }}: {{ job[field[0]] }} </span>
      </div>
    </div>
  </article>
</template>

<script>
import { utilService } from '../services/utilService'

export default {
  props: {
    job: {
      required: true,
      type: Object,
    },
  },

  computed: {
    jobSubfields() {
      const fieldsCopy = { ...this.job }
      delete fieldsCopy.title
      delete fieldsCopy.desc
      delete fieldsCopy.employer
      return Object.entries(fieldsCopy)
    },
  },
  methods: {
    getTranslation: utilService.getTranslation,
    getImgUrl: function getImageUrl(src) {
      return new URL(src, import.meta.url).href
    },
  },
}
</script>
