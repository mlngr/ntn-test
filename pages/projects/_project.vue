<template class="project">
  <section class="project-template">
    <div class="project-template__wrapper">
      <!-- <article v-if="projectPost" class="" v-html="$md.render(projectPost.body)"> -->
      <article v-if="projectPost">
        <section class="header">
          <div class="main-title">
            <h1 class="article-title">{{ projectPost.title }}</h1>
          </div>
          <div class="project-intro">
            <p>
              <!-- <p >{{ projectPost.description }}</p> -->
              We joined forces with our sister studio
              <a title="Algo — Automated videos" href="https://algo.tv" target="_blank" rel="noopener">Algo</a> to
              create the <strong>branding</strong> and <strong>design system</strong> for yet another Bloomberg project:
              a weekly video that mixes live financial data with human curation.
            </p>
          </div>
        </section>
        <div class="project-hero__cover">
          <img
            v-if="projectPost"
            class="cover-image"
            :src="projectPost.cover"
            alt="Maximilien Langonier développeur créatif"
          />
        </div>
        <div class="project-description">
          <div>
            Bloomberg asked us to work our data visualization magic for this automated video campaign analyzing the
            Futures Commodities market. A concise (and eye-catching) financial recap was to be published every Monday,
            right after market closure. It represented a golden opportunity to blend the illo style of design with
            algo’s data-driven solutions in one unique campaign. We brought the vibrant design solutions to an otherwise
            rusty way of representing charts and financial data, while our sister studio kicked in to do the automation
            work. We tried looking at charts from a different perspective in order to achieve a new, bolder look to work
            with data visualization.
          </div>
        </div>
        <div v-if="projectPost.gallery">
          <img v-for="image in projectPost.gallery" class="image-gallery" :key="image.id" :src="image" />
        </div>
        <div class="project-content__credits">
          <p>
            Credits —
            <span
              >Production <u>Luca Gonnelli</u> + Design &amp; Creative Direction <u>Ilenia Notarangelo</u> + Motion
              engineering <u>Matteo Ruffinengo</u> + Data Science <u>Nima Farzaneh</u> + Animation <u>Dave Cubitt</u> +
              Portfolio Case Study &amp; Video <u>Giovanna Crise &amp; Laurentiu Lunic</u></span
            >
          </p>
        </div>
                <div class="project-next">
          <p>découvrir le projet suivant <span style="font-size:0.6em">→</span></p>
          </p>
        </div>
      </article>
    </div>
  </section>
</template>
<script>
export default {
  async asyncData({ params, payload }) {
    if (payload) return { projectPost: payload }
    else
      return {
        projectPost: await require(`~/assets/content/projects/${params.project}.json`),
      }
  },
}
</script>

<style scoped>
.main-title {
  font-family: 'Kobe', sans-serif;
  margin-bottom: 2em;
  font-size: 4em;
  text-align: center;
}

.project-template__wrapper {
  grid-column: 2/12;
  width: 100%;
  margin: 0 auto;
}

.project-intro {
  font-size: 3em;
  font-family: 'Kobe', sans-serif;
  text-align: center;
  line-height: 1.25;
}

.project-hero__cover {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 2em;
}

.project-template {
  overflow: hidden;
  min-height: 100vh;
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-column-gap: 1.875rem;
  padding: 10.625rem 4.10156% 3.75rem;
}

img {
  object-fit: cover;
  width: 100%;
  height: 100%;
}

.image-gallery {
  padding-bottom: 2em;
}
.project-description {
  -moz-columns: 2;
  column-count: 2;
  grid-column-gap: 1.875rem;
  -moz-column-gap: 1.875rem;
  column-gap: 1.875rem;
  margin-bottom: 2em;
  font-size: 2em;
  text-align: left;
  line-height: 1.25;
  font-family: 'Kobe', sans-serif;
  font-weight: 400;
}

.project-content__credits {
  text-align: center;
  font-size: 2.1875rem;
  color: #cdcdcd;
  margin-bottom: 2em;
}

.project-next {
  font-family: 'Kobe', sans-serif;
  font-size: 2em;
  text-align: right;
  color: #cdcdcd;
  margin-top: 4em;
  margin-bottom: 2em;
}
</style>