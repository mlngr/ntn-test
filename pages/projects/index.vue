<template>
  <main
    v-if="projectPosts"
    class="main"
  >
    <h1 class="title text-left">Projets</h1>


    			<div class="gallery gallery-grid"
          v-for="(projectPost, index) in projectPosts"
          :key="index" >
                <nuxt-link
        class=""
        :to="`projects/${projectPost.slug}`"
      >
				<figure class="gallery__item" id="hovergallery">
          <div class="gallery__img-title">
					<div class="gallery__item-img" id="imgform">      
        <img
        v-if="projectPost"
        class="gallery__item-imginner"
        :src="projectPost.coverlisting"
        alt="Maximilien Langonier développeur créatif"
      > 
      </div>

</div>
				</figure>
              <h2 class="gallery__item-title" data-scroll="" data-scroll-speed="2" data-splitting="">{{ projectPost.title }}</h2>

        				<figcaption class="gallery__item-caption">
						<span class="gallery__item-number">01</span>
						<p class="gallery__item-text">{{ projectPost.project_type }}</p>
						<p class="gallery__item-text">1988</p>
					</figcaption>
                </nuxt-link>
			</div>

    <ul
      v-for="(projectPost, index) in projectPosts"
      :key="index"
      class="articles"
    >
      <nuxt-link
        class="article article--clickable"
        :to="`projects/${projectPost.slug}`"
      >
        <h3 class="article-title">{{ projectPost.title }}</h3>
        <div class="mt-4 mb-2">
          <h2 class="inline py-1 px-2 mr-1 bg-accent text-white font-medium rounded-sm dark:bg-accent">{{ projectPost.project_type }}</h2>
          <p class="inline">{{ projectPost.description }}</p>
        </div>
      </nuxt-link>
    </ul>
  </main>
</template>
<script>
export default {
  computed: {
    projectPosts() {
      return this.$store.state.projectPosts
    }
  }
}
</script>

<style scoped>

.title {
	grid-area: content;
	font-size: 15vw;
	margin: 0;
	font-family: ivypresto-headline, serif;
	font-weight: 100;
	justify-self: center;
	align-self: center;
	position: relative;
	z-index: 1500;
	color: #c5681c;
	pointer-events: none;
	width: 100%;
	height: 100vh;
	display: flex;
	align-items: center;
	justify-content: center;
	align-self: start;
}

.gallery {
	grid-area: content;
	justify-self: center;
}

.gallery__item {
    align-items: center;
    justify-content: center;
    align-self: start;
    margin-top: 25vh;
    margin-bottom: 25vh;
  transition: 0.3s;
}


.gallery {
  cursor: pointer;
  transition: 0.3s;
}

.gallery:hover{
transform: scale(1.02);
}




.noscroll .gallery__item-img {
  cursor: default;
  
}


.gallery__item-imginner {
  padding: 24%;
  background-size: cover;
  background-position: 50% 0;
  width: 100%;
  transition: 0.3s;
}

.gallery__item-caption {
	grid-area: gallery-caption;
	padding: 0 0 1rem;
}


.gallery__item-title {
  font-size: 5rem;
  padding: 40px;
  margin-top: -70%;
  z-index: 1;
  /* width: 100%; */
  /* text-align: center; */
  font-family: ivypresto-headline, serif;
  font-weight: 100;
  transition: 0.3s;
} 

.gallery__item-number {
	font-family: ivypresto-headline, serif;
	font-weight: 100;
	font-size: 2.5rem !important;
	border-bottom: 1px solid #494444;
	width: 100%;
	display: block;
	margin-bottom: 1rem;
}

.gallery__item-text {
  margin: 0;
  	font-size: 2.5rem !important;
}

.gallery__item-number,
.gallery__item-text {
  will-change: transform, opacity;
  	font-size: 2.5rem !important;
}

@media screen and (min-width: 53em) {
	.gallery__item {
	}
	.gallery__item-caption {
		padding: 0 0 0 1rem;
	}
}

.gallery-grid {
    align-items: center;
    justify-content: center;
    align-self: start;
}

</style>
