<template>
<div id="content0">
	<div class="container">
		<div id="carousel">
			<figure><img src="./pic/s1.png" alt="" @click="print('1')"></figure>
			<figure><img src="./pic/s2.png" alt="" @click="print('2')"></figure>
			<figure><img src="./pic/s3.png" alt="" @click="print('3')"></figure>
			<figure><img src="./pic/s4.png" alt="" @click="print('4')"></figure>
			<figure><img src="./pic/s5.png" alt="" @click="print('5')"></figure>
			<figure><img src="./pic/s6.png" alt="" @click="print('6')"></figure>
			<figure><img src="./pic/s7.png" alt="" @click="print('7')"></figure>
			<figure><img src="./pic/s8.png" alt="" @click="print('8')"></figure>
			<figure><img src="./pic/s9.png" alt="" @click="print('9')"></figure>
		</div>
	</div>
    <div v-if="notprint">
	  </br></br></br></br></br></br></br></br>
	  <h3>Try to click the picture?</h3>
	</div>
	<!-- 强行加载图片((( -->
	<div v-if="fls">
	  <img src="./pic/1.png">
	  <img src="./pic/2.png">
	  <img src="./pic/3.png">
	  <img src="./pic/4.png">
	  <img src="./pic/5.png">
	  <img src="./pic/6.png">
	  <img src="./pic/7.png">
	  <img src="./pic/8.png">
	  <img src="./pic/9.png">
	</div>

</div>
</template>

<script src="./js/prefixfree.min.js"></script>
<script src='./js/none.js'></script>
<script src="./js/index.js"></script>

<script>
export default{
  name:'content0',

  data () {
	return {
      inform: '',
	  notprint: true,
	  fls: false
	}
  },

  methods:{
	print(arg){
	  var s = './dist/' + arg + '.png';
	  document.getElementById('bigpic').src = s;
	  var s2 = 'Information: This is '+arg+'.png';
	  document.getElementById('textInf').innerHTML=s2;
	  this.notprint=false;
	}
  }
}
</script>

<style src="./css/style.css"></style>