<template>
  <div class="container">
    <Header />
    <ColorModePicker />
    <nuxt />

    <Footer />
  </div>
</template>

<script>
import Header from '~/components/general/Header.vue'
import Footer from '~/components/general/Footer.vue'
import ColorModePicker from '~/components/general/ColorModePicker.vue'

export default {
  components: {
    Header,
    ColorModePicker,
    Footer,
  },
}
</script>
