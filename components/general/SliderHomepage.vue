<template>
  <client-only>
    <section class="slider">
      <swiper :class="theme" :options="swiperOption">
        <swiper-slide class="swiper-slide">
          <div class="wayfx-slide-content">
            <a href="https://koplesh.co/">
              <img
                data-src="https://www.welovegreen.fr/wp-content/uploads/2017/05/edito1-1.jpg"
                class="ls-is-cached lazyloaded"
                alt="Studio Clax - Création et développement de site internets à Nice - KOPLESH - Concerts, agenda paris, musique indé"
                width="800px"
                height="600px"
                v-lazy-load
              />
            </a>
          </div>
        </swiper-slide>
        <swiper-slide class="swiper-slide">
          <div class="wayfx-slide-content">
            <a href="https://crestofficiel.com/">
              <img
                data-src="https://cdn.shopify.com/s/files/1/0476/5945/0520/t/7/assets/21-12-min.jpg?v=16316368296045814457"
                class="ls-is-cached lazyloaded"
                alt="Studio Clax - Création et développement de site internets à Nice - Crest officiel - Mode"
                width="800px"
                height="600px"
                v-lazy-load
              />
            </a>
          </div>
        </swiper-slide>
        <swiper-slide class="swiper-slide">
          <div class="wayfx-slide-content">
            <a href="https://koplesh.co/">
              <img
                data-src="https://cdn.archilovers.com/projects/b_730_326b440a-f905-4a15-b463-7de75480292e.jpg"
                class="ls-is-cached lazyloaded"
                alt="Studio Clax - Création et développement de site internets à Nice - KOPLESH - Concerts, agenda paris, musique indé"
                width="800px"
                height="600px"
                v-lazy-load
              />
            </a>
          </div>
        </swiper-slide>
        <swiper-slide class="swiper-slide">
          <div class="wayfx-slide-content">
            <a href="http://alga.design/">
              <img
                src="https://images.squarespace-cdn.com/content/v1/59875f18d482e9f06c7e959d/1502047829558-Y3ENXTPQYSMMYBSOE0OT/ke17ZwdGBToddI8pDm48kLIj3bb_uLOihttx7hjsPSV7gQa3H78H3Y0txjaiv_0fDoOvxcdMmMKkDsyUqMSsMWxHk725yiiHCCLfrh8O1z4YTzHvnKhyp6Da-NYroOW3ZGjoBKy3azqku80C789l0lqfkVpRp1g_2L-WsTQRP4IUeQvxhQLxDj0GQzUQT21mzi2feheXFTkax-QWHoTYtA/DSC_3378.jpg"
                class="ls-is-cached lazyloaded"
                alt="Studio Clax - Création et développement de site internets à Nice - Alga Samuel Tomatis Design"
                width="800px"
                height="600px"
              />
            </a>
          </div>
        </swiper-slide>
      </swiper>
    </section>
  </client-only>
</template>

<script>
import { directive } from 'vue-awesome-swiper'

export default {
  name: 'SliderHomepage',
  directives: {
    swiper: directive,
  },
  data() {
    return {
      theme: null,
      banners: ['/slider-1.png', 'https://easol.com/images/homepage/testimonials/6.webp'],
      swiperOption: {
        slidesPerView: 'auto',
      },
    }
  },
}
</script>

<style >
.swiper-container {
  position: relative;
  padding-left: 8.2vw;
  cursor: url('https://i.ibb.co/ZJYTs2D/cursor.png'), auto;
  margin: 60px auto;
  padding-top: 0px;
  padding-bottom: 0px;
  -webkit-animation: scroll 60s linear infinite;
  animation: scroll 60s linear infinite;
}

@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(calc(-250px * 7));
  }
}

.swiper-wrapper {
  display: flex !important;
  flex-direction: row;
}

.swiper-slide.swiper-slide-duplicate.swiper-slide-prev {
  margin: auto;
}

.swiper-slide.swiper-slide-next {
  margin: auto;
}

.swiper-slide.swiper-slide-active {
  margin: auto;
}
.swiper-slide {
  font-size: 16px;
  letter-spacing: -0.01em;
  padding: 0 10px;
}

.arrow-next {
  margin-left: 0.5vw;
}

.wayfx-slide-content {
}

.wayfx-slide-content a {
  cursor: url('https://i.ibb.co/ZJYTs2D/cursor.png'), auto;
}

.wayfx-slide-content img {
  height: 600px;
  width: 800px;
  object-fit: cover;
}

img.ls-is-cached:hover {
  opacity: 0.8;
}

@media (max-width: 480px) {
}

@media (max-width: 600px) {
}
</style>