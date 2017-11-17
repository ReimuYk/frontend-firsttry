<template>
<div id="app">
  <div>
    <!--<img src="./pic/test.png" height=400>-->
    <img v-if="isstart === false" src="./assets/logo.png" id="imgtest">
    <h1>{{ msg }}</h1>
    <h2>{{ text1 }}</h2>
    <ul>
      <li><a v-if="showinf" href="javascript:;" @click="ShowInf">Show Information</a></li>
      <li><a v-if="isstart === false" href="javascript:;" @click="Alt">Start!</a></li>
    </ul>
  </div>
  <div v-if="isstart">
    <!-- <img src="./pic/test.png"> -->
    <h1>item1</h1>
    
    <content0></content0>
  </div>
</div>
</template>

<script>
import content0 from "./components/content0.vue"
export default {
  name:'app',
  data () {
    return {
      msg: 'A Simple Picture Scanner',
      text1: 'Vue version 2.0',
      isstart: false,
      showinf: true
    }
  },
  components: {
    content0
  },

  methods:{
      Show(){
        var adres="./dist/test.png";
        document.getElementById('imgtest').src = adres;
      },
      Alt(){
        //document.getElementById('imgtest').src = '';
        this.isstart=true;
        // document.getElementById('imgtest').height = 250;
        // document.getElementById('imgtest').width = 100;
        // alert("alert!");
      },
      ShowInf(){
        this.text1 = "Student ID:516030910257  Name:胡雨奇";
        this.showinf = false;
      }
  }

  
}
function Show(arg){
    alert("arg");
}
</script>





<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
