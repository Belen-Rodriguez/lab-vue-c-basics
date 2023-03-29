<template>
    <h2>Itineration 5</h2>
    <div class="btnContainer">
    <button @click="changeClass" :class="changeColor()" > Change me!
    </button>
    </div>

</template>
    
<script>
export default {
  name: 'FooterComp',
  data() {
    return {
        btnClass: true,
    }
  },
  methods: {
    changeClass(){
        this.btnClass = !this.btnClass
    },
    changeColor(){
      if (this.btnClass) {return 'blueBtn'}
      else {return 'yellowBtn'}
    }
  }
  }


</script>
    
<style scoped>
*{
  text-align: center;
  color: rgb(8, 33, 33);
}

.yellowBtn {
    background-color: yellowgreen;
}
.blueBtn {
    background-color: rgb(79, 101, 160);
}
    
</style>