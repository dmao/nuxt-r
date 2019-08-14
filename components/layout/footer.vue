<template lang="pug">
  footer.p-4
    p.text-gray-500.text-center © {{ currentYear }} Didier Mahaux | 
      a.underline(href="https://www.linkedin.com/in/didier-mahaux-631a2220/", rel="noreferrer noopener", target="_blank") Linkedin
      | 
      a.underline(href="https://github.com/dmao/nuxt-r", rel="noreferrer noopener", target="_blank") Source
</template>

<script>
export default {
  name: 'Footer',
  computed: {
    currentYear() {
      return new Date().getFullYear()
    }
  }
}
</script>
