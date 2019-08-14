<template lang="pug">
  section.mb-16.container.mx-auto.px-4(class="lg:px-16")
    h1.text-center.uppercase.mb-8.text-xl.font-bold Projects
    ul.mb-2
      li.rounded.overflow-hidden.shadow-lg(
        v-for="(project, index) in projectList",
        class="hover:shadow-2xl")
        a(:href="project.url", rel="noreferrer noopener", target="_blank")
          figure
            img(
              :src="`img/clients/${project.slug}.jpg`", 
              :srcset="`img/clients/${project.slug}.jpg 1x, img/clients/${project.slug}-2x.jpg 2x`", 
              loading="lazy", 
              :alt="`screenshot of ${project.name} website.`")
            figcaption.px-4.py-2
              h2.font-bold.text-xl {{ project.name }}
              h3.text-gray-600.text-base {{ project.sector }}
              p.text-sm for {{ project.company }}

</template>

<script>
export default {
  name: 'ClientsWithImages',
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
  grid-gap: 2rem
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr))

a:hover
  background-color: red;
  background-blend-mode: multiply;
</style>
