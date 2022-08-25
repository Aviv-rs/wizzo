<template>
  <section className="card-list">
    <header class="flex space-between">
      <h2 class="bold">{{ title }}</h2>
      <button class="btn-see-all">{{ seeAll }}</button>
    </header>
    <div class="list-container">
      <div v-for="(card, idx) in cards" :key="idx">
        <CardPreview :imgFolder="imgFolder" :card="card" :cardIdx="idx + 1" />
      </div>
    </div>
  </section>
</template>

<script>
import CardPreview from './CardPreview.vue'
export default {
  props: {
    cards: {
      required: true,
      type: Array,
    },
    title: {
      required: true,
      type: String,
    },
    seeAll: {
      required: true,
      type: String,
    },
    imgFolder: {
      required: true,
      type: String,
    },
  },
  components: {
    CardPreview,
  },
}
</script>
