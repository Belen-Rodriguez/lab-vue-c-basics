

<template>
  <h1>Welcome to Muva Architecture</h1>

  <NavBar />
  <PostSection/>
  <BtnChange/>
  <FooterComp />
</template>

<script>
import NavBar from './components/NavBar.vue'
import PostSection from './components/PostSection.vue'
import BtnChange from './components/BtnChange.vue'
import FooterComp from './components/FooterComp.vue'

export default {
  name: 'App',
  data(){
    return {

    }
  },
  components: {
    NavBar,
    PostSection,
    BtnChange,
    FooterComp,
}
}
</script>

<style scoped>
body{
  text-align: center;
}
h1{
  text-align: center;
}
h5{
  font-size: 1.6rem;
}

</style>
