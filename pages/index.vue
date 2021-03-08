<template>
  <div class="main">
    <section class="leader-homepage panel">
      <div class="leader-content">
        <div class="main-text">
          <h1 class="main-title">Studio Clax</h1>
          <h2 class="main-subtitle">{{ homeContent.intro }}</h2>
          <img id="myVideo" src="~/static/placeholder-nice.webp" alt="Studio Clax - Création et développement de site internets à Nice" />
          <video autoplay muted loop id="myVideo">
            <source src="~/static/nice.mp4" type="video/mp4" />
          </video>

          <div class="holder"></div>

          <!-- <a :href="homeContent.buttonLink">
            <button class="button-text-content">{{ homeContent.buttonLabel }}</button>
          </a> -->
          <div class="keywords">
            <span class="keyword">stratégie</span>
            <span class="keyword">désign</span>
            <span class="keyword">développement</span>
            <span class="keyword">performance</span>
          </div>
          <a href="#services">
            <div class="hero-scroll-container">
              <span class="scroll">Scroll</span>
            </div>
          </a>
        </div>
      </div>
      <div class="marquee-container">
        <div class="marquee-wrapper">
          <p class="marquee-text">
            Site en développment&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Mais nous
            sommes ouverts&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; N'hésitez pas à nous
            contacter !&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Site en
            développment&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Mais nous sommes
            ouverts&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; N'hésitez pas à nous
            contacter !&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Site en
            développment&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Mais nous sommes
            ouverts&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; N'hésitez pas à nous
            contacter !&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Site en
            développment&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Mais nous sommes
            ouverts&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; N'hésitez pas à nous
            contacter !&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          </p>
        </div>
      </div>
    </section>
    <section class="whatwedo" @scroll="updateScroll" @mouseenter="lazyLoadImage">
      <div class="content">
        <!-- <h2>Bonjour 👋</h2> -->
        <p class="main-intro">
          Nous sommes une agence numérique établie à Nice, dans le sud de la France. 
          Nous sommes spécialisés dans le développement de solutions numériques basées sur une approche intégrant stratégie, design et technologie.
          
          Du début jusqu’à la mise en ligne, nos projets sont le fruit d’une étroite collaboration entre vous, développeurs, designers et stratèges numériques..
        </p>
      </div>
    </section>

    <section id="DatoCmsSHeadline-11960556-en" ref="my_box_a">
      <span id="services"></span>
      <div class="sc-bdfBwQ UElzp Box-cYgLTd dTLTVs">
        <div class="sc-dlfnbm gQsQBB">
          <div class="sc-hKgILt gALUoe">
            <div class="sc-eCssSg dIcDaN">
              <h2
                class="Text-jAOEoN SectionTitle__StyledSectionTitle-cOxWkj leKkVv fCRuop SectionTitle__StyledSectionTitle-sc-6zpykb-0 section-title"
                font-size="1"
                font-weight="500"
              >
                Les derniers projets qui nous été confiés
              </h2>
            </div>
          </div>
        </div>
      </div>
    </section>
    <div>
      <SliderHomepage />
    </div>

    <section class="whatwedo">
      <div class="content">
        <h2>Ce que nous pouvons vous apporter</h2>
        <p class="main-intro">
          Notre objectif est de transformer les gens en amateurs de marques. Nous suivons l'approche "digital-first".
          Des expériences numériques convaincantes résultent d'une marque bien définie. Grâce à nos outils, nous créons
          des sites web de marque, des applications et des canaux de médias sociaux qui convertissent, que leur objectif
          soit l'information, le commerce électronique, le divertissement ou la communication.
        </p>
        <div class="content-accordion">
          <h3>
            <button v-on:click="toggleStrategy"><span class="accordion-more">+ </span>Stratégie</button>
          </h3>
          <div class="tags" v-show="showStrategy">
            <div>
              <p class="tag-intro">
                Découverte de votre histoire, de vos valeurs et de vos objectifs afin d’élaborer ensemble des stratégies
                - adaptées et efficaces - appuyées par le numérique.
              </p>
              <span class="tag">Stratégie numérique</span><span class="tag">Stratégie de contenu</span>
              <span class="tag">Recherche Utilisateur</span><span class="tag">Atelier centré utilisateur</span><span class="tag">Aterlier d'innovation &amp; d'idéation</span>
              <span class="tag">Positionnement de marque</span>
              <span class="tag">Définition de KPI</span><span class="tag">Audit</span><span class="tag">Roadmap</span>
            </div>
          </div>
          <hr class="service-line"/>
        </div>
        <div class="content-accordion">
          <h3>
            <button v-on:click="toggleDesign"><span class="accordion-more">+ </span>Design</button>
          </h3>
          <div class="tags" v-show="showDesign">
            <p class="tag-intro">
              Nos regards créatifs, toujours à l'affût des aspirations du moment, nous permettent de définir des
              positionnements identitaires, de repenser votre logo, de redéfinir votre charte graphique. Tout en
              déclinant ces choix pour vos produits numériques.
            </p>
            <div>
              <span class="tag">Identité visuelle</span>
              <span class="tag">Charte graphique</span><span class="tag">Création de logo</span><span class="tag">Mise en valeur de vos espaces &amp; produits</span>
              
              <span class="tag">Supports de communication</span><span class="tag">Illustration</span><span class="tag">Animation 2D &amp; 3D</span>
            </div>
          </div>
          <hr class="service-line"/>
        </div>
        <div class="content-accordion">
          <h3>
            <button v-on:click="toggleDev"><span class="accordion-more">+ </span>Création de site web &amp; mobile</button>
          </h3>
          <div class="tags" v-show="showDev">
            <div>
              <span class="tag">Design d'interface (UI)</span><span class="tag">Expérience utilisateur (UX)</span><span class="tag">Prototypage</span><span class="tag">Wireframing</span><span class="tag">Création de boutique e-commerce (Shopify)</span
              ><span class="tag">Système de gestion de contenu (CMS)

</span><span class="tag">Développement Back-end

</span><span class="tag">Développement Front-end

</span><span class="tag">Landing page</span><span class="tag">Portfolio</span>
            </div>
          </div>
          <hr class="service-line"/>
        </div>
        <div class="content-accordion">
          <h3>
            <button v-on:click="toggleConsulting">
              <span class="accordion-more">+ </span>Performance, conseil et accompagnement
            </button>
          </h3>
          <div class="tags" v-show="showConsulting">
            <div>
              <span class="tag">Optimisation en ligne (SEO)</span><span class="tag">Data Analyse</span><span class="tag">Optimisation du taux de conversion (CRO)</span>
              <span class="tag">Recommendation produit</span><span class="tag">Campagne social média</span>
              <span class="tag">Gestion de campagne adwords</span><span class="tag">Gestion du nom de domaine</span> <span class="tag">Formation &amp; accompagnement</span> 
            </div>
          </div>
          <hr class="service-line"/>
        </div>

        <!-- <div class="content-accordion">
          <h3>
            <button v-on:click="toggleStrategy"><span>+</span> Design</button>
          </h3>
          <transition
            name="accordion"
            v-on:before-enter="beforeEnter"
            v-on:enter="enter"
            v-on:before-leave="beforeLeave"
            v-on:leave="leave"
          >
            <div class="tags" v-show="showStrategy">
              <div>
                <span class="tag">Analytics</span><span class="tag">Consulting</span>
                <span class="tag">User Research</span><span class="tag">Innovation &amp; Ideation</span>
                <span class="tag">Business Integration</span><span class="tag">Content Strategy</span>
                <span class="tag">Service Design</span><span class="tag">SEO Strategy</span>
              </div>

              <hr class="service-line"/>
            </div>
          </transition>
        </div> -->
      </div>
    </section>
    <div class="test" v-observe-visibility="visibilityChanged" >
      <!-- <section>
        <section id="DatoCmsSHeadline-11960556-en">
          <span id="services"></span>
          <div class="sc-bdfBwQ UElzp Box-cYgLTd dTLTVs">
            <div class="sc-dlfnbm gQsQBB">
              <div class="sc-hKgILt gALUoe">
                <div class="sc-eCssSg dIcDaN">
                  <h2 class="section-title panel">Une palette pluridisciplinaire au service de vos projets</h2>
                </div>
              </div>
            </div>
          </div>
        </section> -->
        <!-- 
      <section class="section-two-column">
        <div class="dontknow1">
          <div class="content-video-text">
            <div class="dontknow2">
              <div class="content-video">
                <div class="content-image">
                  <img
                    src="https://www.datocms-assets.com/38511/1611231359-01-testanywhre-anytimeposter.jpg"
                    alt="Maximilien Langonier développeur créatif"
                    class="hDwyTD"
                  />
                </div>
              </div>
              <div class="content-bloc-text">
                <div class="content-bloc-text-title">
                  <h2 class="content-bloc-text-title-h2">01. Stratégie</h2>
                </div>
                <p class="content-bloc-text-p">
                  Découverte de votre histoire, de vos valeurs et de vos objectifs afin d’élaborer ensemble des
                  stratégies - adaptées et efficaces - appuyées par le numérique.
                </p>
                <div class="content-bloc-text-button">
                  <a title="Remote Testing" href="/"
                    ><button name="Remote Testing" class="button-text-content">
                      <div class="content-button-text-content">Découvrir nos services</div>
                    </button></a
                  >
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
                  <img
                    src="https://studioplastac.fr/v3/wp-content/uploads/2020/12/gloria-plastac-papeterie-06.jpg"
                    alt="Maximilien Langonier développeur créatif"
                    class="hDwyTD"
                  />
                </div>
              </div>
              <div class="content-bloc-text">
                <div class="content-bloc-text-title">
                  <h2 class="content-bloc-text-title-h2">02. Design</h2>
                </div>
                <p class="content-bloc-text-p">
                  Nos regards créatifs, toujours à l'affût des aspirations du moment, nous permettent de définir des
                  positionnements identitaires, de repenser votre logo, de redéfinir votre charte graphique. Tout en
                  déclinant ces choix pour vos produits numériques.
                </p>
                <div class="content-bloc-text-button">
                  <a title="Remote Testing" href="/"
                    ><button name="Remote Testing" class="button-text-content">
                      <div class="content-button-text-content">Découvrir notre démarche UX</div>
                    </button></a
                  >
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section class="section-two-column">
        <div class="dontknow1">
          <div class="content-video-text">
            <div class="dontknow2">
              <div class="content-video">
                <div class="content-image">
                  <img
                    src="https://www.5-5.paris/public_data/savoir/1518618584/40-27/2048/studio55-savoirfaire-identite-siteinternet2.jpg"
                    alt="Maximilien Langonier développeur créatif"
                    class="hDwyTD"
                  />
                </div>
              </div>
              <div class="content-bloc-text">
                <div class="content-bloc-text-title">
                  <h2 class="content-bloc-text-title-h2">03. Contenu</h2>
                </div>
                <p class="content-bloc-text-p">
                  Comment mettre en avant vos produits, votre lieu ou vos équipes sans du contenu à la hauteur ? Nous
                  collaborons avec des photographes professionnels capables de mettre en lumière tous vos projets.
                </p>
                <div class="content-bloc-text-button">
                  <a title="Remote Testing" href="/"
                    ><button name="Remote Testing" class="button-text-content">
                      <div class="content-button-text-content">Découvrir nos services</div>
                    </button></a
                  >
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
                  <img
                    src="https://images.unsplash.com/photo-1587127936972-ebdd135de438?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=2027&q=80"
                    alt="Maximilien Langonier développeur créatif"
                    class="hDwyTD"
                  />
                </div>
              </div>
              <div class="content-bloc-text">
                <div class="content-bloc-text-title">
                  <h2 class="content-bloc-text-title-h2">04. Site internet</h2>
                </div>
                <p class="content-bloc-text-p">
                  Notre force ? Concevoir des sites internets esthétiques, rapides et ergonomiques. Sur lesquels vous et
                  vos équipes seront autonomes pour gérer votre contenu.
                </p>
                <div class="content-bloc-text-button">
                  <a title="Remote Testing" href="/"
                    ><button name="Remote Testing" class="button-text-content">
                      <div class="content-button-text-content">Découvrir nos services</div>
                    </button></a
                  >
                </div>
              </div>
            </div>
          </div>
        </div>
      </section> -->
      </section>

      <section class="collaborate">
        <p class="collaborate-first-word">Un projet? <span class="collaborate-second-word"> Parlons-en!</span></p>
        <p></p>
      </section>
    </div>
  </div>
</template>


<script>
import SliderHomepage from '~/components/general/SliderHomepage.vue'

export default {
  async asyncData({ payload }) {
    if (payload) return { homeContent: payload }
    else
      return {
        homeContent: await require(`~/assets/content/site/homepage.json`),
      }
  },
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    }
  },
  data: function () {
    return {
      scrollPosition: null,
      showStrategy: false,
      showDesign: false,
      showDev: false,
      showConsulting: false,
    }
  },
  methods: {
    // updateScroll() {
    //   this.scrollPosition = window.scrollY
    //   console.log(this.scrollPosition)
    // },
    lazyLoadImage(e) {
      let media = e.target.parentNode.querySelectorAll('[data-manual-lazy]')
      ;[...media].forEach((m) => this.$lazyLoad(m))
    },
    visibilityChanged(isVisible, entry) {
      let header = document.querySelector('.test')
      if ((header.isVisible = isVisible)) {
        header.classList.add('v-toolbar--bgchange')
      }
    },
    updateScroll() {
      this.scrollPosition = window.scrollY
    },
    toggleStrategy: function () {
      this.showStrategy = !this.showStrategy
    },
    toggleDesign: function () {
      this.showDesign = !this.showDesign
    },
    toggleDev: function () {
      this.showDev = !this.showDev
    },
    toggleConsulting: function () {
      this.showConsulting = !this.showConsulting
    },
    // enter: function(el, done) {
    //   $(el).slideDown(150, done);
    // },
    // leave: function(el, done) {
    //   $(el).slideUp(150, done);
    // },
    beforeEnter: function (el) {
      el.style.height = '0'
    },
    enter: function (el) {
      el.style.height = el.scrollHeight + 'px'
    },
    beforeLeave: function (el) {
      el.style.height = el.scrollHeight + 'px'
    },
    leave: function (el) {
      el.style.height = '0'
    },
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll)
  },
  components: {
    SliderHomepage,
  },
  destroyed() {
    window.removeEventListener('scroll', this.updateScroll)
  },
}
</script>

<style scoped>
/* .v-toolbar--bgchange {
  background: rgb(137, 186, 209);
  color: rgb(141, 62, 52);
  transition: background-color 3s ease;
} */
section {
  margin-bottom: 10%;
}
section.whatwedo {
  max-width: 1920px;
  margin: 0px auto 8em;
  width: calc(100% - (3.6923rem + 6.4103vw));
  display: flex;
  flex-direction: column;
  padding-bottom: calc(1.8462rem + 3.2051vw);
}

section.whatwedo .content {
  text-align: left;
  margin-left: 16.66%;
  width: 66.66%;
  box-sizing: border-box;
  padding: calc(0.5385rem + 1.2821vw);
  -webkit-box-flex: unset;
  flex-grow: unset;
}

section.whatwedo h2 {
  font-family: 'Kobe', sans-serif;
  letter-spacing: 0.2px;
  font-size: calc(1.3231rem + 2.4359vw);
  line-height: 1.4;
  margin: 0px 0px 0.5em -0.05em;
  margin-top: 0px;
  margin-right: 0px;
  margin-bottom: 0.5em;
  margin-left: -0.05em;
}

section.whatwedo p.main-intro {
  margin-top: 2em;
  margin-bottom: 1.5em;
  font-size: calc(1.1231rem + 0.7692vw);
  line-height: calc(2.2308rem + 1.0256vw);
}

section.whatwedo p.tag-intro {
  margin-top: 2em;
  margin-bottom: 2em;
  font-size: 20px;
  line-height: 32px;
}

section.whatwedo h3 {
  position: relative;
  font-size: 3rem;
  margin-top: 1.5rem;
  margin-bottom: 1rem;
}

section.whatwedo button {
  font-size: 2rem;
  border: none;
  background-image: initial;
  background-color: transparent;
  color: inherit;
  border-color: initial;
  outline-color: initial;
  margin: 0px;
  padding: 0px;
  outline: 0px;
  text-align: left;
  cursor: pointer;
}

.tag {
  display: inline-block;
  font-size: 1.2rem;
  letter-spacing: 0.04em;
  border: 1px solid;
  border-radius: 6em;
  padding: 0.6em 1.6em;
  margin: 0px 0.6em 1em 0px;
  transition: all 0.6s ease 0s;
  white-space: nowrap;
}

section.whatwedo .tags {
  margin-bottom: 2em;
  margin-top: 2em;
  transition: ease-in 2s;
}

.accordion-more {
}

h1 {
  font-family: Kobe, sans-serif;
  font-size: 10rem;
}

#myVideo {
  z-index: -1;
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  height: 100vh;
  width: 100%;
  object-fit: cover;
}

.section-two-column {
  position: relative;
}

.dontknow1 {
  position: relative;
  max-width: 1440px;
  box-sizing: border-box;
  min-width: 0px;
  margin: 60px auto;
  padding-top: 0px;
  padding-bottom: 0px;
}

.idontknow3 {
  width: auto;
  margin-right: auto;
  margin-left: auto;
  padding-right: 2rem;
  padding-left: 2rem;
}

.content-video-text {
  margin-right: auto;
  margin-left: auto;
}

.dontknow2 {
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

.content-image {
  padding-right: 2rem;
  padding-left: 2rem;
}

.content-bloc-text {
  flex-basis: 41.6667%;
  max-width: 41.6667%;
  display: block;
  box-sizing: border-box;
  flex: 0 0 auto;
  padding-right: 2rem;
  padding-left: 2rem;
}

.content-bloc-text {
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

.content-bloc-text-title {
  box-sizing: border-box;
  margin: 0px 0px 30px;
  min-width: 0px;
}

h2.content-bloc-text-title-h2 {
  line-height: 1.2;
  text-transform: none;
  overflow: unset;
  white-space: unset;
  text-overflow: unset;
}

p.content-bloc-text-p {
  font-size: 18px;
  font-weight: 400;
  line-height: 1.5;
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

.button-text-content {
  display: inline-flex;
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

.light-mode .button-text-content {
  background-color: var(--bg-light);
  color: var(--secondary-color-light);
  border: 2px solid var(--secondary-color-light);
}

.dark-mode .button-text-content {
  background-color: var(--bg-dark);
  color: var(--secondary-color-dark);
  border: 2px solid var(--secondary-color-dark);
}

.light-mode .button-text-content:hover {
  background-color: var(--main-color-light);
  color: var(--secondary-color-dark);
  box-shadow: rgb(20 26 40 / 15%) 0px 10px 60px;
}

.dark-mode .button-text-content:hover {
  background-color: var(--bg-light);
  color: var(--secondary-color-light);
  box-shadow: rgb(20 26 40 / 15%) 0px 10px 60px;
}

section.leader-homepage {
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  align-self: start;
  background-color: #1e344a;
  color: white;
}

.leader-content {
  z-index: 1;
}

.row-reverse {
  flex-flow: row-reverse wrap;
}

.main-text {
}

.gALUoe {
  -webkit-box-pack: center;
  justify-content: center;
  box-sizing: border-box;
  display: flex;
  flex: 0 1 auto;
  flex-flow: row wrap;
  margin-right: -2rem;
  margin-left: -2rem;
}

.hero-scroll-container {
  padding: 30px;
}

.hero-scroll-container {
  position: absolute;
  bottom: 0px;
  right: 0;
  padding: 3.3333333333vh 2.0833333333vw;
  width: auto;
  box-sizing: border-box;
  z-index: 4;
  text-align: right;
}

.hero-scroll-container .scroll::after {
  content: ' ↓';
}

.hero-scroll-container .scroll:after {
  display: block;
}

.hero-scroll-container .scroll {
  color: var(--white);
  display: inline-block;
  text-align: center;
  cursor: pointer;
}

h2.section-title {
  font-family: Kobe, sans-serif;
  padding: 20px;
  letter-spacing: 0.2px;
  font-size: 6rem;
  margin-top: 0;
  margin-bottom: 0;
}

hr.service-line {
  border: 1px solid;
}

@media (min-width: 1600px) {
  /* .UElzp {
    margin-top: 160px;
    margin-bottom: 160px;
  } */

  section {
    padding: 60px;
  }

  .gQsQBB {
    width: 132rem;
  }

  .dIcDaN {
    flex-basis: 66.6667%;
    max-width: 66.6667%;
    display: block;
  }

  .section-title {
    font-size: 4.4rem;
  }

  .collaborate-first-word {
    font-size: 6rem;
  }
}

@media (min-width: 1024px) and (max-width: 1599px) {
  .content-video-text {
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

  .dontknow1 {
    margin-top: 140px;
    margin-bottom: 140px;
  }

  .section-title {
    font-size: 3.4rem;
  }

  /* .UElzp {
    margin-top: 160px;
    margin-bottom: 160px;
  } */

  .dIcDaN {
    flex-basis: 66.6667%;
    max-width: 66.6667%;
    display: block;
  }

  .collaborate-first-word {
    font-size: 6rem;
  }

  .collaborate-second-word {
    font-size: 6rem;
  }
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

  .main-title {
    font-size: 72px;
  }

  .main-subtitle {
    font-size: 24px;
  }

  h2.section-title {
    font-size: 3rem;
  }

  h2.section-title.panel {
    height: auto !important;
  }

  section {
    padding: 20px;
  }

  .collaborate-first-word {
    font-size: 3.2rem;
  }

  .collaborate-second-word {
    font-size: 3.2rem;
  }

  section.whatwedo .content {
    width: 100%;
    margin: 0;
    padding: 0;
  }

  section.whatwedo p.main-intro {
    font-size: 18px;
    line-height: 30px;
  }

  .keyword {
    font-size: 14px;
  }

  .hero-scroll-container {
    display: none;
  }

  .h2-sans---450.contact-button {
    font-size: 14px !important;
  }
}

section.collaborate {
  text-align: center;
  word-break: keep-all;
  padding: 20px;
  letter-spacing: 0.2px;
  font-size: 6rem;
  margin-bottom: 0;
}

.arrow-contact {
  transform: rotateY(180deg);
  display: inline-block;
}

.svg-max {
  width: 180px;
  pointer-events: none;
  bottom: -10px;
  right: 20px;
  animation-name: rotation;
  animation-duration: 4s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  -webkit-animation: rotation 4s infinite linear;
}

.light-mode .svg-max {
  fill: black;
}

.dark-mode .svg-max {
  fill: white;
}

@-webkit-keyframes rotation {
  0% {
    -webkit-transform: rotate(280deg);
  }
  50% {
    -webkit-transform: rotate(380deg);
  }
  100% {
    -webkit-transform: rotate(280deg);
  }
}

.collaborate-second-word {
  font-weight: bold;
  font-family: 'Kobe', sans-serif;
  letter-spacing: 0.2px;
}

/* Setting fade transition and default settings */
body {
  transition: background-color 1s ease;
}

/* panel styles */
.panel {
  /* min height incase content is higher than window height */
  height: 100vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.change_color {
  background-color: rgb(247, 247, 234);
  color: rgb(13, 102, 167);
  -webkit-transition: all 1s ease-in-out;
  -o-transition: all 1s ease-in-out;
  transition: all 1s ease-in-out;
}

/* marquee slider */

.marquee-container {
  max-width: 100%;
  overflow: hidden;
  text-transform: uppercase;
  z-index: 1;
  top: 0;
  position: absolute;
  background-color: rgb(65, 109, 128);
  color: rgb(148, 217, 247);
}

.marquee-wrapper {
  width: 100vw;
  white-space: nowrap;
}

.marquee-text {
  font-size: 18px;
  display: inline-block;
  will-change: transform;
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
</style>