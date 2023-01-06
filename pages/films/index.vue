<template lang="pug">
  main
    h1 Films
    ul.film-grid
      li(v-for="film in films")
        nuxt-link(:to="`/films/${film.slug}`")
          img(:src="film.filmStills" :alt="film.title")
          p.film-title {{ film.title }}
</template>

<script>
export default {
  async asyncData({ $content }) {
    const films = await $content('films').fetch()
    return { films }
  }
}
</script>