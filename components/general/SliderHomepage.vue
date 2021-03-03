<template>
  <section class="slider">
    <swiper :class="theme" :options="swiperOption">
      <swiper-slide class="swiper-slide">
        <div class="wayfx-slide-content">
          <a href="https://shop.immieats.com/products/spicy-beef-ramen/">
            <img
              src="https://www.welovegreen.fr/wp-content/uploads/2017/05/edito1-1.jpg"
              class="ls-is-cached lazyloaded"
              alt=""
            />
          </a>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <div class="wayfx-slide-content">
          <a href="https://shop.immieats.com/products/spicy-beef-ramen/">
            <img
              src="https://cdn.shopify.com/s/files/1/0476/5945/0520/t/7/assets/21-12-min.jpg?v=16316368296045814457"
              class="ls-is-cached lazyloaded"
              alt=""
            />
          </a>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <div class="wayfx-slide-content">
          <a href="https://shop.immieats.com/products/spicy-beef-ramen/">
            <img
              src="https://cdn.archilovers.com/projects/b_730_326b440a-f905-4a15-b463-7de75480292e.jpg"
              class="ls-is-cached lazyloaded"
              alt=""
            />
          </a>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <div class="wayfx-slide-content">
          <a href="https://shop.immieats.com/products/spicy-beef-ramen/">
            <img
              src="https://images.squarespace-cdn.com/content/v1/59875f18d482e9f06c7e959d/1502047829558-Y3ENXTPQYSMMYBSOE0OT/ke17ZwdGBToddI8pDm48kLIj3bb_uLOihttx7hjsPSV7gQa3H78H3Y0txjaiv_0fDoOvxcdMmMKkDsyUqMSsMWxHk725yiiHCCLfrh8O1z4YTzHvnKhyp6Da-NYroOW3ZGjoBKy3azqku80C789l0lqfkVpRp1g_2L-WsTQRP4IUeQvxhQLxDj0GQzUQT21mzi2feheXFTkax-QWHoTYtA/DSC_3378.jpg"
              class="ls-is-cached lazyloaded"
              alt=""
            />
          </a>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </section>
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
      banners: ['/slider-1.png', 'https://easol.com/images/homepage/testimonials/6.webp'],
      swiperOption: {
        allowTouchMove: true,
        loop: true,
        slidesPerView: '2',
        spaceBetween: 40,
        navigation: {
          nextEl: '.button-next',
          prevEl: '.button-prev',
        },
        breakpoints: {
          1024: {
            slidesPerView: 3,
            spaceBetween: 40,
          },
          768: {
            slidesPerView: 3,
            spaceBetween: 20,
          },
          640: {
            slidesPerView: 2,
            spaceBetween: 20,
          },
          320: {
            slidesPerView: 1,
            spaceBetween: 10,
          },
        },
      },
    }
  },
}
</script>

<style >
section.slider {
  position: inherit;
  max-width: 100%;
  min-height: 100vh;
  display: contents;
}

.swiper-container {
  position: relative;
  padding-left: 8.2vw;
  cursor: url('https://i.ibb.co/ZJYTs2D/cursor.png'), auto;
  position: relative;
  max-width: 1440px;
  box-sizing: border-box;
  min-width: 0px;
  margin: 60px auto;
  padding-top: 0px;
  padding-bottom: 0px;
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
  object-fit: cover;
  height: 400px;
  width: 300px;
}

img.ls-is-cached:hover {
  opacity: 0.8;
}

@media (max-width: 480px) {
  .wayfx-slide-content__info {
    flex-wrap: wrap;
    margin-top: 40px;
  }
  .product-button {
    flex: 1;
    margin-top: 32px;
  }

  .product-description {
    max-width: 80%;
    margin: auto;
  }

  .wayfx-slide-content img {
    height: 67.467vw;
    width: 100%;
    margin: 0 auto 32px;
  }

  .swiper-slide-active .wayfx-slide-content a {
    transform: scale(0.8);
  }

  .swiper-button-prev {
    left: 16px;
    bottom: unset;
    top: 27%;
  }
  .swiper-button-next {
    right: 16px;
    bottom: unset;
    top: 27%;
  }
}

@media (max-width: 600px) {
  .wayfx-slide-content {
    max-width: 90%;
    margin: auto;
  }

  .wayfx-slide-content img {
    max-width: 400px !important;
    height: 400px !important;
  }
}

.slider-arrows {
  display: flex;
  align-items: center;
  position: absolute;
  bottom: 0;
  left: 0;
}

.arrow {
  width: 2.778vw;
  height: 2.778vw;
}
</style>