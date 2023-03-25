

<template>
  <h1>APP Page</h1>
  <p>{{ newMsg }}</p>
  <NavBar />
  <PostSection />
  <FooterComp />
</template>

<script>
import NavBar from './components/NavBar.vue'
import PostSection from './components/PostSection.vue'
import FooterComp from './components/FooterComp.vue'

export default {
  name: 'App',
  data(){
    return {
      newMsg: 'Hola',
    }
  },
  components: {
    NavBar,
    PostSection,
    FooterComp,
}
}
</script>

<style scoped>

</style>
