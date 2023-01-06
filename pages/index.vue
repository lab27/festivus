<template lang="pug">
  main
    .tower-wrapper.cols-12
      img(src="/img/tower.svg", alt="Gåsebäck Film Festival Hero Image")
</template>

<script>
export default {
  head () {
    return {
      title: 'Home',
      bodyAttrs: {
        class: 'page-home'
      }
    }
  }, 
  mounted() {
    console.log('index page mounted');
    this.$emit('indexPageLoaded')
  }
}
</script>

<style>
.tower-wrapper {
  position: relative;
  height: 100vh;
  overflow: hidden;
  display: grid;
  place-content: center;
}

.tower-wrapper img {
  height: 70vh;
}
</style>

