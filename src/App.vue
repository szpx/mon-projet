<template>
  <contenu></contenu>
  <header-top></header-top>
</template>
<script>

import Contenu from './components/Contenue.vue'
import Header from './components/Header.vue'
export default {
  name: 'App',
  components: {
      'contenu': Contenu,
      'header-top': Header
  }
}
</script>

<style>
</style>
