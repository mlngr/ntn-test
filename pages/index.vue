<template>
  <div class="main">
    <section class="leader-homepage">
    <p class="main-title">ONADA 🏖</p>
    <h2 class="main-subtitle">This website will become an agency portfolio template</h2>
    </section>
  </div>
</template>

<script>
// import Logo from '~/components/Logo.vue'

export default {
  // components: {
  //   Logo
  // },
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }]
    }
  }
}
</script>

<style scoped>
h1 {
font-size: 10rem;
}
</style>