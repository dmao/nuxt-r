<template lang="pug">
  nav
    NLink(to="/") Home
    NLink(to="/clients") Clients
</template>

<script>
export default {
  name: 'Navigation'
}
</script>

<style>
nav {
  @apply flex items-center justify-between flex-wrap bg-blue-700 p-6;
}
</style>
