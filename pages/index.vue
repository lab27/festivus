<template lang="pug">
  main
    p This is the Vesuvian Man
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
  },




}
</script>

