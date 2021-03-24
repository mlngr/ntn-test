<template class="slider">
  <client-only>
    <swiper :options="swiperOption">
      <swiper-slide class="swiper-slide">
        <div class="wayfx-slide-content">
          <a href="https://crestofficiel.com/" target="_blank">
            <img
              src="https://cdn.shopify.com/s/files/1/0476/5945/0520/t/7/assets/21-12-min.jpg?v=16316368296045814457"
              alt="Studio Clax - Création et développement de site internets à Nice - Crest officiel - Mode"
              width="500px"
              height="600px"
              v-lazy-load
            />
          </a>
          <h2 class="featured-project__title">Crest Officiel</h2>
          <p class="featured-project__description">Création du site internet / E-commerce</p>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <div class="wayfx-slide-content">
          <a href="https://koplesh.co/" target="_blank">
            <img
              src="https://koplesh.co/3.jpg"
              alt="Studio Clax - Création et développement de site internets à Nice - KOPLESH - Concerts, agenda paris, musique indé"
              width="500px"
              height="600px"
              v-lazy-load
            />
            <h2 class="featured-project__title">KOPLESH</h2>
            <p class="featured-project__description">Stratégie / Développement / Direction Artistique</p>
          </a>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <div class="wayfx-slide-content">
          <a>
            <img
              src="https://cdn.archilovers.com/projects/b_730_326b440a-f905-4a15-b463-7de75480292e.jpg"
              alt="Studio Clax - Création et développement de site internets à Nice - KOPLESH - Concerts, agenda paris, musique indé"
              width="500px"
              height="600px"
              v-lazy-load
            />
            <h2 class="featured-project__title">Architecture Giraldi - <span style="font-size: 1rem">WIP</span></h2>
            <p class="featured-project__description">Création du site internet / Accompagnement</p>
          </a>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <div class="wayfx-slide-content">
          <a href="http://alga.design/" target="_blank">
            <img
              src="https://images.squarespace-cdn.com/content/v1/59875f18d482e9f06c7e959d/1502047829558-Y3ENXTPQYSMMYBSOE0OT/ke17ZwdGBToddI8pDm48kLIj3bb_uLOihttx7hjsPSV7gQa3H78H3Y0txjaiv_0fDoOvxcdMmMKkDsyUqMSsMWxHk725yiiHCCLfrh8O1z4YTzHvnKhyp6Da-NYroOW3ZGjoBKy3azqku80C789l0lqfkVpRp1g_2L-WsTQRP4IUeQvxhQLxDj0GQzUQT21mzi2feheXFTkax-QWHoTYtA/DSC_3378.jpg"
              alt="Studio Clax - Création et développement de site internets à Nice - Alga Samuel Tomatis Design"
              width="500px"
              height="600px"
              v-lazy-load
            />
          </a>
          <h2 class="featured-project__title">Samuel Tomatis - Alga</h2>
          <p class="featured-project__description">Création du site internet / Stratégie digitale</p>
        </div>
      </swiper-slide>

      <div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div>
    </swiper>
  </client-only>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'

export default {
  name: 'SliderHomepage',
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      swiperOption: {
        slidesPerView: 'auto',
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
        keyboard: {
          enabled: true,
        },
      },
    }
  },
}
</script>

<style >
.slider {
}
.swiper-slide {
  width: auto;
  height: auto;
  position: relative;
  /* -webkit-animation: scroll 60s linear infinite;
  animation: scroll 60s linear infinite; */
}

.swiper-container {
  /* cursor: url('https://i.ibb.co/ZJYTs2D/cursor.png'), auto; */
  padding-top: 0px;
  padding-bottom: 0px;
  padding-left: 60px;
}

@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(calc(-250px * 2));
  }
  100% {
    transform: translateX(0);
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
  text-align: left;
}

/* .wayfx-slide-content a {
  cursor: url('https://i.ibb.co/ZJYTs2D/cursor.png'), auto;
} */

.wayfx-slide-content img {
  object-fit: cover;
}

.featured-project__title {
  margin: 0;
  font-size: 1.5rem;

  font-weight: 800;
  /* color: #1f1f1f;
    font-family: 'Noto Serif TC', serif; */
}

.featured-project__description {
  margin: 0;
  margin-top: 0.25rem;
  font-size: 1rem;
  opacity: 0.6rem;
  /* color: #707070; */
  font-family: 'Kobe', sans-serif;
}

img.ls-is-cached:hover {
  opacity: 0.8;
}

@media (min-width: 1600px) {
  .wayfx-slide-content img {
    height: 600px;
    width: 400px;
    margin-bottom: 1rem;
  }
}

@media (min-width: 1024px) and (max-width: 1599px) {
  .wayfx-slide-content img {
    height: 500px;
    width: 350px;
    margin-bottom: 1rem;
  }
}

@media (min-width: 900px) and (max-width: 1023px) {
  .wayfx-slide-content img {
    height: 400px;
    width: 300px;
  }
}

@media (min-width: 640px) and (max-width: 899px) {
  .wayfx-slide-content img {
    height: 450px;
    width: 300px;
  }

  .swiper-container {
    padding-left: 0px;
  }

  .featured-project__title {
    margin-top: 0.25rem;
    font-size: 1.25rem;
  }
}

@media (min-width: 0px) and (max-width: 639px) {
  .wayfx-slide-content img {
    height: 400px;
    width: 250px;
  }

  .swiper-container {
    padding-left: 0px;
  }

  .featured-project__title {
    margin-top: 0.25rem;
    font-size: 1rem;
  }
}
</style>