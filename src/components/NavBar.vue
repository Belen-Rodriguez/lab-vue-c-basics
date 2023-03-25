<template>
  <h2>Nav Component</h2>
  <p>{{ navMsg }}</p>
  <p>{{ sum }}</p>
  <p>{{ allProjects() }}</p>
  <p>{{ firstProject() }}</p>
  <p v-if="firstProject() === 'project01' ">Yes it is the same!</p>
  <p v-else>No, it is not the same!</p>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      navMsg: 'Hello Nav',
      sum: 2 + 2,
      menu: {
        home: 'About us',
        projects: ['project01', 'project02', 'project03'],
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

<style scoped></style>
