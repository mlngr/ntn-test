<template>
  <nav class="">
    <ul class="flex fixed top-0 inset-x-0 p-3">
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
  name: 'Header'
}
</script>

<style lang="postcss" scoped>

.flex-1{
flex: 1 1 0%;
} 

.fixed {
    position: fixed;
    right: 0;
    left: 0;
    top: 0;
    padding: 0 0.75rem;
    display: flex;
}

</style>
