<template lang="pug">
  div
    About
    Skills
    ClientsWithImages
    ClientsList


</template>

<script>
import About from '~/components/complex/about.vue'
import Skills from '~/components/complex/skills.vue'
import ClientsWithImages from '~/components/complex/clientsWithImages.vue'
import ClientsList from '~/components/complex/clientsList.vue'

export default {
  name: 'Clients',
  components: {
    About,
    Skills,
    ClientsWithImages,
    ClientsList
  }
}
</script>
