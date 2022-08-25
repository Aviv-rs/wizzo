<template>
  <section className="card-list">
    <CardPreview v-for="card in cards" :key="card._id" :card="card" />
  </section>
</template>

<script>
import CardPreview from './CardPreview.vue'
export default {
  emits: ['cardRemoved'],
  props: {
    cards: {
      required: true,
      type: Array,
    },
  },
  components: {
    CardPreview,
  },
}
</script>
