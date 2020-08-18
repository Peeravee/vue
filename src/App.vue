<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
   <!--<br />   <img alt="bg" src="./assets/12.jpg" /><br />-->
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <h1>{{button}}</h1>
    
      

      <div class="col-3"><counter lable="Start" @cc="sum" /></div> 
      <div class="col-3"><counter lable="Attack" @cc="sum" /></div>
      <div class="col-3"><counter lable="Specia" @cc="sum" /></div>
      <div class="col-3"><counter lable=" Attack " @cc="sum" /></div>
 




</div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Counter from "./components/Counter.vue";
export default {
  name: "App",
  components: {
    HelloWorld,
    Counter,
  },
  data: function(){
    return{
      total: 0,
      name:'',
      code:'',
      gpa:'0.0',
  }
  },
methods : {
  // 3. 
  sum(counterValue){
    this.total += counterValue
   
  },

},

};
</script>

<style>
body{
  background-image: url(https://blogs-images.forbes.com/erikkain/files/2019/05/endgame-1.jpg)
  
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>