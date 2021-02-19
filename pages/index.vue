<template>
  <div class="main">
    <section class="leader-homepage">
    <div class="leader-content">
      <div class="main-text">
    <p class="main-title">ONADA 🏖</p>
    <h2 class="main-subtitle">This website will become an agency portfolio template</h2>
      </div>
    </div>
    </section>

      <section class="section-two-column">
        <div class="dontknow1">
            <div class="content-video-text">
              <div class="dontknow2">
              <div class="content-video">
            <div class="content-image">
            <img src="https://www.datocms-assets.com/38511/1611231359-01-testanywhre-anytimeposter.jpg" class="hDwyTD">
            </div>
            </div> 
              <div class="content-bloc-text"> 
                <div class="content-bloc-text-title">         
                <h2 class="content-bloc-text-title-h2">Test anywhere, anytime</h2>
                </div>
                <p class="content-bloc-text-p">Easily create a maze for every project need, from usability tests to user surveys, then share with users in a matter of minutes with a simple URL. </p>
                <div class="content-bloc-text-button">
                  <a title="Remote Testing" href="/platform/user-testing/"><button name="Remote Testing" class="button-text-content">
                    <div class="content-button-text-content">Learn more</div></button></a>
                </div>
              </div>
              </div>
            </div>
        </div>
      </section>
      

      <section class="section-two-column">
        <div class="dontknow1">
            <div class="content-video-text">
              <div class="dontknow2 row-reverse">
              <div class="content-video">
            <div class="content-image">
            <img src="https://images.unsplash.com/photo-1613591733452-811c8e40bc99?ixid=MXwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHw1OXx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=60" class="hDwyTD">
            </div>
            </div> 
              <div class="content-bloc-text"> 
                <div class="content-bloc-text-title">         
                <h2 class="content-bloc-text-title-h2">Test anywhere, anytime</h2>
                </div>
                <p class="content-bloc-text-p">Easily create a maze for every project need, from usability tests to user surveys, then share with users in a matter of minutes with a simple URL. </p>
                <div class="content-bloc-text-button">
                  <a title="Remote Testing" href="/platform/user-testing/"><button name="Remote Testing" class="button-text-content">
                    <div class="content-button-text-content">Learn more</div></button></a>
                </div>
              </div>
              </div>
            </div>
        </div>
      </section>
  </div>
</template>

<script>
// import Logo from '~/components/Logo.vue'

export default {
  // components: {
  //   Logo
  // },
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }]
    }
  }
}
</script>

<style scoped>
h1 {
font-size: 10rem;
}

.section-two-column {
    position: relative;
}

.dontknow1{
      position: relative;
    max-width: 1440px;
    box-sizing: border-box;
    min-width: 0px;
    margin: 60px auto;
    padding-top: 0px;
    padding-bottom: 0px;
}

.idontknow3{
    width: auto;
    margin-right: auto;
    margin-left: auto;
    padding-right: 2rem;
    padding-left: 2rem;
}

.content-video-text{
    margin-right: auto;
    margin-left: auto;
}

.dontknow2{
  box-sizing: border-box;
    display: flex;
    flex: 0 1 auto;
    flex-flow: row wrap;
    margin-right: -2rem;
    margin-left: -2rem;
    -webkit-box-pack: center;
    justify-content: center;
    -webkit-box-align: center;
    align-items: center;
}


.content-video {
flex-basis: 50%;
    max-width: 50%;
    display: block;
        box-sizing: border-box;
    flex: 0 0 auto;
}

.content-image{
    padding-right: 2rem;
    padding-left: 2rem;  
}

.content-bloc-text{
    flex-basis: 41.6667%;
    max-width: 41.6667%;
    display: block;
        box-sizing: border-box;
    flex: 0 0 auto;
    padding-right: 2rem;
    padding-left: 2rem;
}

.content-bloc-text{
    font-size: 28px;
    box-sizing: border-box;
    margin: 0px;
    min-width: 0px;
    padding-top: 5px;
    padding-bottom: 5px;
    text-align: left;
}

img.hDwyTD {
    margin: auto;
    display: block;
    position: relative;
    width: 100%;
    max-height: 600px;
    border-radius: 20px;
    object-fit: cover;
}

.content-bloc-text-title{
  box-sizing: border-box;
  margin: 0px 0px 30px;
  min-width: 0px;
}

h2.content-bloc-text-title-h2{
    line-height: 1.2;
    font-family: Roobert, sans-serif;
    text-transform: none;
    overflow: unset;
    white-space: unset;
    text-overflow: unset;
}

p.content-bloc-text-p{
      font-size: 18px;
    font-weight: 400;
    line-height: 1.5;
    font-family: "Public Sans", sans-serif;
    text-transform: none;
    overflow: unset;
    white-space: unset;
    text-overflow: unset;
}

.content-bloc-text-button {
  box-sizing: border-box;
  margin: 30px 0px 0px;
  min-width: 0px;
}

.button-text-content{
  display: inline-flex;
    font-family: "Public Sans", sans-serif;
    -webkit-box-align: center;
    align-items: center;
    font-weight: 600;
    white-space: nowrap;
    font-size: 16px;
    -webkit-box-pack: center;
    justify-content: center;
    text-decoration: none;
    cursor: pointer;
    appearance: none;
    padding: 16px 36px;
    line-height: 24px;
    border-radius: 36px;
    box-sizing: border-box;
    transition: all 0.2s ease-in-out 0s;
    box-shadow: none;
}

.light-mode .button-text-content{
  background-color: var(--bg-light);
  color: var(--secondary-color-light); 
  border: 2px solid var(--secondary-color-light);
}

.dark-mode .button-text-content{
    background-color: var(--bg-dark);
    color: var(--secondary-color-dark); 
    border: 2px solid var(--secondary-color-dark);
}

.light-mode .button-text-content:hover{
    background-color: var(--main-color-light);
    color: var(--secondary-color-dark);
    box-shadow: rgb(20 26 40 / 15%) 0px 10px 60px;
}

.dark-mode .button-text-content:hover{
    background-color: var(--bg-light);
    color: var(--secondary-color-light);
    box-shadow: rgb(20 26 40 / 15%) 0px 10px 60px;
}

section.leader-homepage{
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  align-self: start;
}

.row-reverse{
  flex-flow: row-reverse wrap;;
}

.main-text{
}

@media (min-width: 1024px) and (max-width: 1600px) {

.content-video-text{
  width: 1320px;
}
.content-bloc-text {
    margin-left: 6.333%;
    flex-basis: 33.3333%;
    max-width: 33.3333%;
    display: block;
}

.content-video {
    flex-basis: 41.6667%;
    max-width: 41.6667%;
    display: block;
}

.dontknow1{
    margin-top: 140px;
    margin-bottom: 140px;
}

}

@media (min-width: 1024px) {

}

@media (min-width: 900px) and (max-width: 1023px) {

.dontknow1 {
    margin-top: 100px;
    margin-bottom: 100px;
}


}

@media (min-width: 640px) and (max-width: 899px) {

.content-video {
    flex-basis: 80%;
    max-width: 80%;
}

.content-bloc-text {
    flex-basis: 80%;
    max-width: 80%;
}

.content-bloc-text {
    font-size: 24px;
}

}

@media (min-width: 0px) and (max-width: 639px) {

.content-video {
    flex-basis: 90%;
    max-width: 90%;
}

.content-bloc-text {
    flex-basis: 90%;
    max-width: 90%;
}

.dontknow1 {
    margin-top: 60px;
    margin-bottom: 60px;
}

.content-bloc-text {
    font-size: 22px;
}
}


</style>