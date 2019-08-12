<template lang="pug">
  section
    h1 Clients
    ul.mb-2
      li.rounded.overflow-hidden.shadow-lg(v-for="(project, index) in projectList")
        a(:href="project.url", rel="noreferrer noopener", target="_blank")
          figure
            img(:src="`img/clients/${project.slug}.jpg`")
            figcaption.px-4.py-2
              h2.font-bold.text-xl {{ project.name }}
              h3.text-gray-600.text-base {{ project.sector }}
              p.text-sm for {{ project.company }}
    div(v-for="(projet2) in projects")
      p {{ projet2.clientName }} 
      p sector: {{ projet2.projectList.sector }}

</template>

<script>
export default {
  name: 'Clients',
  data() {
    return {
      projects: [
        {
          clientName: 'Emakina',
          projectList: {
            name: 'BNP Baribas',
            sector: 'bank'
          }
        },
        {
          clientName: 'TenTwelve',
          projectList: {
            name: '1',
            sector: '2'
          }
        }
      ],
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
  grid-gap: 2rem
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr))
</style>
