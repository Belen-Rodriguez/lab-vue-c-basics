<template>
  <h2>Post Component</h2>
  <p v-for="eachPost in post" :key="eachPost.id"
  >{{ eachPost.title }}</p>
  <p v-for="eachPost in post" :key="eachPost.id"
  >{{ eachPost.content }}</p>
</template>

<script>
export default {
  name: 'PostSecion',
  data() {
    return {
      post: [{
        id: '01',
        title: '01 CONCRETE ARCH',
        description: 'Different uses of concrete in Arch',
        content: ['con structure', 'con façades', 'con finishes' ],
      },
      { 
        id: '02',
        title: '02 WOOD ARCH',
        description: 'Different uses of wood in Arch',
        content: ['wood structure', 'wood façades', 'wood finishes', 'carpentry', 'wood isolation' ],
      },
      {
        id: '02',
        title: '03 METAL ARCH',
        description: 'Different uses of metal in Arch',
        content: ['metal structure', 'metal work'],
      },
    ]
    }
    },

  method: {
    filterPost(){

    }
  },
  }
  

</script>

<style scoped>
h2, p{
  color: darkblue;
}
</style>