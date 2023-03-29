<template>
  <h2>{{ItinerationMsg }}</h2>
  <p>{{ `Sumar ${number1} + ${number2} = ${SumNumbers()}` }}</p>

  <h2>Itineration 4 </h2>
  <h3>Discover our fantastic projects: </h3>
  <div class="postContainer">
  <div v-for="eachPost in post" :key="eachPost.id" class="postArticles">
    <article >
  <p >{{ eachPost.title }}</p>
  <p >{{ eachPost.description }}</p>
  <p v-for="eachContent in eachPost.content" :key="eachContent.id" 
  >{{ eachContent }}</p>
    </article>
 
</div>
</div>
</template>

<script>

export default {
  name: 'PostSecion',
  
  data() {
    return {
      ItinerationMsg: 'Itineration 2',
      number1: 2,
      number2: 3,
      post: [{
        id: '01',
        title: 'CONCRETE ARCH',
        description: 'Different uses of concrete in Arch',
        content: ['concrete structure', 'concrete façades', 'concrete finishes' ],
      },
      { 
        id: '02',
        title: 'WOOD ARCH',
        description: 'Different uses of wood in Arch',
        content: ['wood structure', 'wood façades', 'wood finishes', 'carpentry', 'wood isolation' ],
      },
      {
        id: '03',
        title: 'METAL ARCH',
        description: 'Different uses of metal in Arch',
        content: ['metal structure', 'metal work'],
      },
    ]
    }
    },

  methods: {
    SumNumbers(){
    return this.number1 + this.number2}
    }

  }

  

</script>

<style scoped>
*{
  text-align: center;
  color: darkblue;
}

h2{
  font-size: 1.5rem;
  margin-top: 2rem;
}
.contentProject {
  display:inline;
  display: flex;
  flex-direction: row;
  align-items: center;
  text-align: center;
}
.postArticles{

  background-color: rgb(236, 252, 247);
  width: 28%;

}
.postContainer{
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  margin: 2rem 0rem;
}

</style>