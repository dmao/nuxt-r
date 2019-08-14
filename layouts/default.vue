<template lang="pug">
  div.bg-gray-100
    main
      nuxt
    Footer

</template>

<script>
import Footer from '~/components/layout/footer.vue'

export default {
  components: {
    Footer
  }
}
</script>

<style>
html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto,
    'Helvetica Neue', Arial, sans-serif;
  font-size: 1rem;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
</style>
