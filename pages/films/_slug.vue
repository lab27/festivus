<template lang="pug">
  main.film-detail
    h1 {{ film.title }}
    p.film-header-meta dir. {{ film.director }} / {{ film.type }} / {{ film.durationInMinutes }} min
    .film-content
      img(:src="film.filmStills", alt="", srcset="")
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const film = await $content('films', params.slug).fetch()
    return { film }
  },
  head() {
    return {
      title: this.film.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.film.description
        }
      ]
    }
  }
}
</script>