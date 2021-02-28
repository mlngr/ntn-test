<template>
  <nav class="">
    <ul class="flex top-nav top-0 inset-x-0 p-3">
      <li class="flex-1 mr-2">
        <nuxt-link class="btn block" to="/">Home</nuxt-link>
      </li>
      <li class="flex-1">
        <nuxt-link class="btn block" to="/projects">Projets</nuxt-link>
      </li>
    </ul>
    <a href="mailto:m.langonier@gmail.com" class="menu_link_button w-inline-block">
      <h3 class="h2-sans---450 contact-button">Un projet ? Contactez-nous</h3></a
    >
  </nav>
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
  margin-top: 0px;
  border-style: solid;
  border-width: 1px;
  border-color: #ac4e29;
  border-radius: 80px;
  background-color: #ac4e29;
  text-decoration: none;
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
</style>
