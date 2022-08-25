<template>
  <section class="home-page flex column main-layout">
    <hero></hero>
    <cardList
      :cards="articles"
      :title="'עדכונים וחדשות'"
      :seeAll="'לכל העדכונים והחדשות'"
      imgFolder="news-and-updates"
    ></cardList>
    <cardList
      :cards="events"
      :title="'אירועים קרובים'"
      :seeAll="'לכל האירועים'"
      imgFolder="events"
    ></cardList>

    <JobList :jobs="jobs"></JobList>
  </section>
</template>

<script>
import JobList from '@/cmps/JobList.vue'
import CardList from '@/cmps/CardList.vue'
import Hero from '@/cmps/Hero.vue'
import { jobs, articles, events } from '@/data'
export default {
  components: { Hero, CardList, JobList },
  data() {
    return {
      articles,
      events,
      jobs,
    }
  },
}
</script>
