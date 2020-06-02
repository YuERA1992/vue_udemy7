<template>
  <div id="app">
    <!-- <p>{{message}}</p>
    <input type="text" v-model="message"> -->
    <!-- <input type="text" v-model="m">m
    <br>
    <input type="text" v-model="km">km
    <br>
    <input type="text" v-model="mm">mm -->
    <!-- firstName:<input type="text" v-model="firstName" />
    <br>
    lastName:<input type="text" v-model="lastName"/>
    <p>fullName:{{firstName}} {{lastName}}</p> -->
    <ul>
      <li v-for="color in colors" :key="color">
        {{color.name}}</li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      // message:"はじめの値やで"
      // m: 0,
      // km: 0,
      // mm: 0
      // firstName:"",
      // lastName:"",
      colors:[
        {name: "Red"},
        {name: "Blue"},
        {name: "Green"}
      ]  
    }
  },
  computed:{
    

  },
  watch:{
    colors:{
      handler(newValue,oldValue){
        console.log("Update!")
        console.log("new:%s, oldValue: %s",
          JSON.stringify(newValue,null,"\t"),
          JSON.stringify(oldValue,null,"\t")
        )
      },
      deep:true
    }
    // watch:{
    //   firstName(){
    //     return
    //   },
    //   lastName(){
    //     return
    //   }
    
    // km(value){
    //   console.log(value)
    //   this.km=value
    //   this.m=value*1000
    //   this.km=value*1000000
    // },
    // m(value){
    //   console.log(value)
    //   this.km=value/1000
    //   this.m=value
    //   this.km=value*1000
    // },
    // mm(value){
    //   console.log(value)
    //   this.km=value/1000000
    //   this.m=value/1000
    //   this.km=value
    // }
    // message(newValue,oldValue){
    //   console.log ("new: %s, old: %s",newValue,oldValue)
    // }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
