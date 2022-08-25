<template>
  <article className="card-preview flex column">
    <img
      className="card-img"
      :src="`src/assets/imgs/${imgFolder}/` + cardIdx + '.png'"
      alt="card image"
    />
    <time v-if="!!card.time">{{ card.time }}</time>
    <p class="card-content bold">{{ card.content }}</p>
  </article>
</template>

<script>
export default {
  props: {
    card: {
      required: true,
      type: Object,
    },
    cardIdx: {
      required: true,
      type: Number,
    },
    imgFolder: {
      required: true,
      type: String,
    },
  },
}
</script>
