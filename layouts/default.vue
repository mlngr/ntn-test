<template >
  <!-- <div class="container" :class="{ change_color: scrollPosition > 1300 && scrollPosition < 5000 }"> -->
  <div
    class="container"
    :class="{ change_color: scrollPositionRelative < 80, change_color_2: scrollPositionRelative < 30 }"
  >
    <div
      ref="point"
      :style="cursorPoint"
      :class="[
        'g-cursor__point',
        { 'g-cursor_hover': hover },
        { 'g-cursor_click': clickCursor },
        { 'g-cursor_hide': hideCursor },
      ]"
    ></div>
    <Header />

    <!-- Switch between and light mode <ColorModePicker /> -->
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
      xChild: 0,
      yChild: 0,
      xParent: 0,
      yParent: 0,
      hover: false,
      hideCursor: true,
      clickCursor: false,
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
    moveCursor(e) {
      this.xChild = e.clientX - 15
      this.yChild = e.clientY - 15
      setTimeout(() => {
        this.xParent = e.clientX - 15
        this.yParent = e.clientY - 15
      }, 100)
    },
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll)
    window.addEventListener('scroll', this.scrollToBottom)
    window.addEventListener('resize', this.handleResize)
    document.addEventListener('mousemove', this.moveCursor)
    // document.addEventListener('mouseenter', (e) => {
    //   document.querySelector('.custom-hover').style.cursor = 'none'
    //   this.hover = true
    //   console.log('on hover screen')
    // })
    // document.querySelector('.scroll').addEventListener('mouseout', (e) => {
    //   this.hover = false
    //   console.log('ouuut hover screen')
    // })
    document.addEventListener('mouseleave', (e) => {
      this.hideCursor = true
    })
    document.addEventListener('mouseenter', (e) => {
      this.hideCursor = false
    })
    document.addEventListener('click', (e) => {
      this.clickCursor = true
      console.log('event')
      setTimeout(() => {
        this.clickCursor = false
      }, 200)
    })
  },
  computed: {
    cursorPoint() {
      return `transform: translateX(${this.xChild}px) translateY(${this.yChild}px) translateZ(0) translate3d(0, 0, 0);`
    },
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

/* cursor */

.g-cursor__point {
  top: 0;
  left: 0;
  right: 0;
  position: fixed;
  width: 30px;
  height: 30px;
  pointer-events: none;
  border-radius: 100%;
  background: #fff;
  mix-blend-mode: difference;
  z-index: 2;
  cursor: none;
}
.g-cursor_hover {
  top: 0;
  left: 0;
  right: 0;
  position: fixed;
  width: 60px;
  height: 60px;
  /* pointer-events: none; */
  user-select: none;
  border-radius: 100%;
  background: #fff;
  z-index: 55555555;
  backface-visibility: hidden;
  will-change: transform;
  border: 2px solid rgb(255, 255, 255);
  border-radius: 100%;
  z-index: 5555;
  mix-blend-mode: normal;
}

.g-cursor_hide {
  opacity: 0;
  transition: width 0.6s ease, height 0.6s ease, opacity 0.6s ease;
}

.g-cursor_click {
  top: 0;
  left: 0;
  position: fixed;
  width: 26px;
  height: 26px;
  cursor: none;
}
</style>
