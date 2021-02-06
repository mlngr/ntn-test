<template>
  <article
    v-if="jobPost"
    class="main article"
  >
    <h1 class="article-title">{{ jobPost.title }}</h1>
    <h6
      v-if="jobPost.date"
      class="inline-block py-1 px-2 my-2 bg-accent text-white font-medium rounded-sm dark:bg-accent whitespace-no-wrap"
    >{{ formatDate(jobPost.date) }}</h6>
    <div v-html="$md.render(jobPost.body)" />
  </article>
</template>
<script>
export default {
  async asyncData({ params, payload }) {
    if (payload) return { jobPost: payload }
    else
      return {
        jobPost: await require(`~/assets/content/job/${params.job}.json`)
      }
  },
  methods: {
    formatDate(dateString) {
      const date = new Date(dateString)
      return date.toLocaleDateString(process.env.lang) || ''
    }
  }
}
</script>
