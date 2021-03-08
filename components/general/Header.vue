<template>
  <!-- <nav class="">
    <a class="menu_link_left"> <img src="~/static/icon.png" /> </a>
    <ul class="flex top-nav top-0 inset-x-0 p-3">
      <li class="flex-1 mr-2">
        <nuxt-link class="btn block" to="/">Home</nuxt-link>
      </li>
      <li class="flex-1">
        <nuxt-link class="btn block" to="/projects">Projets</nuxt-link>
      </li>
    </ul>
    <a href="mailto:m.langonier@gmail.com" class="menu_link_button">
      <h3 class="h2-sans---450 contact-button">Un projet ? Contactez-nous</h3></a
    >
  </nav> -->
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="postcss" scoped>
.menu_link_button {
  position: absolute;
  top: 32px;
  right: 24px;
  border-radius: 80px;
  background: rgb(18, 84, 241);
  background: linear-gradient(128deg, rgba(18, 84, 241, 1) 0%, rgba(192, 117, 236, 1) 100%);
  text-decoration: none;
  z-index: 2;
}

.menu_link_left {
  position: absolute;
  top: 32px;
  left: 24px;
  z-index: 2;
}

.h2-sans---450.contact-button {
  padding-right: 16px;
  padding-left: 16px;
  -webkit-transform: translate(0px, 0px);
  -ms-transform: translate(0px, 0px);
  transform: translate(0px, 0px);
  text-align: center;
  font-weight: 400;
}

img {
  width: 48px;
}

@media (min-width: 0px) and (max-width: 639px) {
  .h2-sans---450.contact-button {
    font-size: 14px;
  }
}
</style>
