<template>
  <article className="card-preview flex column">
    <img
      className="card-img"
      :src="getImgUrl('../assets/imgs/' + imgFolder + '/' + cardIdx + '.png')"
      alt="card image"
    />
    <div class="info-container">
      <time v-if="!!card.time">{{ card.time }}</time>
      <p class="card-content bold">{{ card.content }}</p>
    </div>
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
  methods: {
    getImgUrl: function (src) {
      return new URL(src, import.meta.url).href
    },
  },
}
</script>
