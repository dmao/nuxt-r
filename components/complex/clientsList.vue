<template lang="pug">
  section.mb-12
    h1.text-center.uppercase.mb-8.text-xl.font-bold 
      span.font-normal More 
      | projects
    div.justify-center.flex-wrap(class="sm:flex")
      div.mx-4.mb-4(v-for="(project) in projects")
        h2.uppercase.border-b-2.border-gray-200.mb-4 
          a(:href="project.clientUrl") {{ project.clientName }}
        ul
          li(v-for="listByclient in project.projectList")
            a.link(:href="listByclient.url") {{ listByclient.name }}
            |  – {{ listByclient.sector }}

</template>

<script>
export default {
  name: 'ClientsList',
  data() {
    return {
      projects: [
        {
          clientName: 'Emakina',
          clientUrl: 'https://emakina.be/',
          projectList: [
            {
              name: 'BNP Baribas',
              url: 'https://www.bnpparibasfortis.be/portal/Start_BE_F.asp',
              sector: 'Bank'
            },
            {
              name: 'Electrabel',
              url: 'https://www.electrabel.be/',
              sector: 'Energy'
            },
            {
              name: 'Deutsche Bank',
              url: 'https://www.deutschebank.be/fr/home-prospect.html',
              sector: 'Bank'
            },
            {
              name: 'Belgacom',
              url: 'https://www.proximus.be/fr/personal.html',
              sector: 'Telephony'
            }
          ]
        },
        {
          clientName: 'TenTwelve',
          clientUrl: 'https://www.tentwelve.com/en',
          projectList: [
            {
              name: 'Fondation A Stichting',
              url: 'http://www.fondationastichting.be/',
              sector: 'Cultural'
            },
            {
              name: 'Cédric Charlier',
              url: 'http://www.cedric-charlier.com/',
              sector: 'Fashion'
            },
            {
              name: 'Tess Store',
              url: 'https://www.boutiquetess.be/',
              sector: 'Store'
            },
            {
              name: 'Zoom Architecture',
              url: 'http://www.zoomarchitecture.be',
              sector: 'Architecture'
            }
          ]
        }
      ]
    }
  }
}
</script>

<style scoped>
.link {
  @apply text-blue-500;
}
</style>
