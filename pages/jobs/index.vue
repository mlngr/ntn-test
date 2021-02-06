<template>
  <main
    v-if="jobPosts"
    class="main"
  >
    <h1 class="title text-left">Jobs</h1>
    <ul
      v-for="(jobPost, index) in jobPosts"
      :key="index"
      class="articles"
    >
      <nuxt-link
        :to="`job/${jobPost.slug}`"
        class="article article--clickable"
      >
        <div class="flex justify-between align-baseline">
          <h3 class="article-title">{{ jobPost.title }}</h3>
          <h6
            v-if="jobPost.date"
            class="inline-block py-1 px-2 bg-accent text-white font-medium rounded-sm dark:bg-accent whitespace-no-wrap"
          >{{ formatDate(jobPost.date) }}</h6>
        </div>
        <div class="mt-4 mb-2">
          <p class="inline">{{ jobPost.description }}</p>
        </div>
      </nuxt-link>
    </ul>
  </main>
</template>
<script>
export default {
  computed: {
    jobPosts() {
      return this.$store.state.jobPosts
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
