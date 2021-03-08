<template>
  <footer id="footer">
    <hr />
    <div class="footer-content">
      <p class="footer-text">© 2021</p>
      <p class="footer-text">design et développement</p>
      <p class="footer-text">Nice, France</p>
      <p><a class="footer-text" href="mailto:m.langonier@gmail.com">contact</a></p>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style lang="css" scoped>
#footer {
  padding-left: 5%;
  padding-right: 5%;
  margin-top: 160px;
  position: relative;
  width: -webkit-fill-available;
  z-index: 1;
  text-align: center;
}

.footer-content {
  overflow: hidden;
  font-family: 'Work Sans', sans-serif;
  font-size: 2rem;
  letter-spacing: -1px;
  font-weight: 100;
  text-transform: lowercase;
  display: flex;
  justify-content: space-between;
}

hr {
  display: block;
  margin: 1em 0;
  padding: 0;
  height: 1px;
  border: 0;
  border-top: 1.5px solid;
}

@media (min-width: 0px) and (max-width: 639px) {
  .footer-content {
    font-size: 1.5rem;
    flex-direction: column;
    text-align: left;
  }

  .footer-text {
    margin: 5px;
  }
}
</style>
