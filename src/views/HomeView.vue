<template>
  <section class="home-page flex column main-layout">
    <hero></hero>
    <card-list
      :cards="articles"
      :title="'עדכונים וחדשות'"
      :seeAll="'לכל העדכונים והחדשות'"
      imgFolder="news-and-updates"
    ></card-list>
    <card-list
      :cards="events"
      :title="'אירועים קרובים'"
      :seeAll="'לכל האירועים'"
      imgFolder="events"
    ></card-list>
  </section>
</template>

<script>
import CardList from '../cmps/CardList.vue'
import Hero from '../cmps/Hero.vue'
export default {
  components: { Hero, CardList },
  data() {
    return {
      articles: [
        {
          content: 'כל התמונות ממסיבת פתיחת סמסטר ב’ תשפ”ב!',
        },
        {
          content: 'רוצה להיות חלק מהאגודה? זו ההזדמנות שלך להשפיע!',
        },
        {
          content: 'הטבות מטורפות למופעי בידור באתר קסטיליה הפקות',
        },
        {
          content:
            'לאחר הודעת המכללה: מספר נקודות לגבי מתווה, החזרה ללימודים פרונטליים',
        },
      ],
      events: [
        {
          content: 'FUNJOYA 2022',
          time: new Intl.DateTimeFormat('he').format(new Date()),
        },
        {
          content: 'יום הסטודנט',
          time: new Intl.DateTimeFormat('he').format(new Date()),
        },
        {
          content: 'סטנדאפ / אסף יצחקי',
          time: new Intl.DateTimeFormat('he').format(new Date()),
        },
        {
          content: 'חוגגים מימונה',
          time: new Intl.DateTimeFormat('he').format(new Date()),
        },
      ],
    }
  },
}
</script>
