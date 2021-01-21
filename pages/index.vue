<template>
  <div>{{ articles }}</div>
</template>

<script>
export default {
  computed: {
    articles() {
      return this.$store.getters['article/articles']
    },
  },

  created() {
    this.$store.dispatch('article/fetchArticles')
  },
}
</script>
