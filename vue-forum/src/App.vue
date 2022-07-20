<template>
  <HeaderOne title=" Hello vue" />
  <!-- <iCargoTitle /> -->
  <MainContent />
</template>

<script>

import HeaderOne from './components/Header.vue'
// import iCargoTitle from './components/Title.vue'
import MainContent from './components/MainContent.vue'
export default {
  name: 'App',
  components: {
    HeaderOne,
    // iCargoTitle,
    MainContent

  }
}
</script>

