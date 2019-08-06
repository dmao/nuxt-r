<template lang="pug">
  section
    h1 Clients
    ul
      li(v-for="(project, index) in projectList")
        a(:href="project.url", rel="noreferrer noopener", target="_blank")
          img(:src="`img/clients/${project.slug}.jpg`")
          h2 {{ project.name }}
          h3 {{ project.sector }}
          p for {{ project.company }}
</template>

<script>
export default {
  name: 'Clients',
  data() {
    return {
      projectList: [
        {
          name: 'Kaboo',
          slug: 'kaboo',
          company: 'GIG',
          sector: 'iGaming',
          url: 'https://www.kaboo.com'
        },
        {
          name: 'Thrills',
          slug: 'thrills',
          company: 'GIG',
          sector: 'iGaming',
          url: 'https://www.thrills.com'
        },
        {
          name: 'SuperLenny',
          slug: 'superlenny',
          company: 'GIG',
          sector: 'iGaming',
          url: 'http://www.superlenny.com'
        },
        {
          name: 'Heritage',
          slug: 'heritage',
          company: 'Afreak',
          sector: 'Fashion',
          url: 'http://heritage-wax.com/fr/heritage'
        },
        {
          name: 'Eastman',
          slug: 'eastman',
          company: 'TenTwelve',
          sector: 'Dance',
          url: 'http://www.east-man.be/fr/'
        },
        {
          name: 'Wiels',
          slug: 'wiels',
          company: 'TenTwelve',
          sector: 'Museum',
          url: 'http://www.wiels.org/'
        },
        {
          name: 'Macs',
          slug: 'macs',
          company: 'TenTwelve',
          sector: 'Museum',
          url: 'http://www.mac-s.be/'
        },
        {
          name: 'Baxter',
          slug: 'baxter',
          company: 'Emakina',
          sector: 'Medical',
          url: 'http://www.baxter.be/fr/index.html'
        },
        {
          name: 'ING',
          slug: 'ing',
          company: 'Emakina',
          sector: 'Bank',
          url: 'https://www.ing.be/en/retail/'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
ul
  display: grid
  grid-gap: 1rem
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr))

li
  outline: 1px solid pink
</style>
