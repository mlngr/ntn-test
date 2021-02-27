<template>
  <nav class="">
    <ul class="flex top-nav top-0 inset-x-0 p-3">
      <li class="flex-1 mr-2">
        <nuxt-link class="btn block" to="/">Home</nuxt-link>
      </li>
      <li class="flex-1">
        <nuxt-link class="btn block" to="/projects">Projets</nuxt-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="postcss" scoped>
</style>
