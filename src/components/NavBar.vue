<template>
  <div class="navBar">
  <h4>{{ navMsg }}</h4>
  <nav v-for="project in menu.projects" :key="project.value"
  >{{ project }}</nav>
  </div>
  <h2>Itineration 3</h2>
  <h5>{{ `See our exclusive projects of ${firstProject()}` }}</h5>
  <p v-if="firstProject() === 'concrete' ">Yes! Our new concrete technology!</p>
  <p v-else>Ond others materials too!</p>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      navMsg: 'Projects:',

      menu: {
        home: 'About us',
        projects: ['concrete', 'wood', 'metal'],
        contact: 'Get in contact!'
      }
    }
  },
  methods: {
    allProjects() {
      return this.menu.projects
    },
    firstProject() {
        return this.menu.projects[0]
    }
  }
}
</script>

<style scoped>
*{
  text-align: center;
}

.navBar{
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.navBar h4{
  width: 40%;
} 
.navBar nav{
  width: 60%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
h2{
  margin-top:2rem;
}



</style>
