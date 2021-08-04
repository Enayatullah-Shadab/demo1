/* eslint-disable no-unused-vars */
<template>
 
  <h1> <img alt="Vue logo" src="./assets/logo.png">ue Demo</h1>
  <h2>{{name}}</h2>
  <p> {{state.value}} </p>
  <button @click="count">Click me</button>


</template>

<script>
import {reactive} from "vue"

export default{
  setup(){
   
    // eslint-disable-next-line no-unused-vars
    const state = reactive({
      value: 0
    })
    
    return{
      name: "Shadab",
      state,
      // value:0,
      count(){
        state.value++
        console.log("Clicked  "+ state.value)
      }

    }
  }
}
</script>
<style>

#app{
  text-align: center;
}
img{
  height: 1em;
}

</style>