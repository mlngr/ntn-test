<template >
  <!-- <div class="container" :class="{ change_color: scrollPosition > 1300 && scrollPosition < 5000 }"> -->
  <div
    class="container"
    :class="{ change_color: scrollPositionRelative < 80, change_color_2: scrollPositionRelative < 20 }"
  >
    <Header />
    <ColorModePicker />
    <nuxt />
    <Footer />
    <!-- <h3 style="position: fixed; top: 0; z-index: 100000">
      Width: {{ window.width }} px<br />
      Height: {{ window.height }} px<br />
      % : {{ scrollPositionRelative }} px<br />
      Height site: {{ site.height }} px<br />
      width site: {{ site.width }} px
    </h3> -->
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
      site: {
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
      this.site.width = document.body.scrollWidth
      this.site.height = document.body.scrollHeight
    },
    scrollToBottom() {
      this.scrollPositionRelative = ((document.body.scrollHeight - window.scrollY) / document.body.scrollHeight) * 100
    },
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll)
    window.addEventListener('scroll', this.scrollToBottom)
    window.addEventListener('resize', this.handleResize)
  },
  destroyed() {
    window.removeEventListener('scroll', this.updateScroll)
    window.removeEventListener('scroll', this.scrollToBottom)
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
