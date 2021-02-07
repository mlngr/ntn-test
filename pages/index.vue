<template>
  <div class="main text-center flex flex-col items-center justify-center">
    <!-- <logo /> -->
    <h1 class="title">ONADA 🏖</h1>
    <h2 class="subtitle">This website will become an agency portfolio template</h2>
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