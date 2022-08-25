<template>
  <RouterLink :to="`/card/${card._id}`">
    <article className="card-preview flex align-center">
      <img className="avatar" src="../assets/imgs/card-default.png" alt="" />
      <h4 class="card-name">{{ card.name }}</h4>
    </article>
  </RouterLink>
</template>

<script>
export default {
  props: {
    card: {
      required: true,
      type: Object,
    },
  },
  emits: ['cardSelected'],
}
</script>
