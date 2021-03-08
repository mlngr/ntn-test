<template >
  <!-- <div class="container" :class="{ change_color: scrollPosition > 1300 && scrollPosition < 5000 }"> -->
  <div class="container" :class="{ change_color: scrollPosition > 1300, change_color_2: scrollPosition > 4000 }">
    <Header />
    <ColorModePicker />
    <nuxt />
    <Footer />
    <h3 style="position: fixed; top: 0; z-index: 100000">
      Width: {{ window.width }} px<br />
      Width % : {{ scrollPositionRelative }} px<br />
      Height: {{ window.height }} px
    </h3>
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
  data: function () {
    return {
      scrollPosition: null,
      window: {
        width: null,
        height: null,
      },
      scrollPositionRelative: null,
    }
  },
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY
    },
    handleResize() {
      this.window.width = window.innerWidth
      this.window.height = window.innerHeight
    },
    scrollToBottom() {
      this.scrollPositionRelative = window.innerWidth - window.scrollY
      console.log(this.scrollPositionRelative)
    },
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll)
    window.addEventListener('resize', this.handleResize)
  },
  destroyed() {
    window.removeEventListener('scroll', this.updateScroll)
    window.removeEventListener('resize', this.handleResize)
  },
}
</script>

<style >
.change_color {
  background-color: rgb(247, 247, 234);
  color: rgb(13, 102, 167);
  -webkit-transition: all 1s ease-in-out;
  -o-transition: all 1s ease-in-out;
  transition: all 1s ease-in-out;
}

.change_color_2 {
  background: rgb(137, 186, 209);
  color: rgb(141, 62, 52);
  -webkit-transition: all 1s ease-in-out;
  -o-transition: all 1s ease-in-out;
  transition: all 1s ease-in-out;
}
</style>
