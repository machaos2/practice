<template>
  <div id="app">
  	<Header/>
  	<div class="container">
  		<router-view/>
  	</div>
  	<Footer/>
  	<vue-canvas-nest :config="{color:'0,50,90', count: 88, opacity:0.8 ,pointColor: '255, 155, 0', zIndex: -1}"></vue-canvas-nest>
  </div>
</template>

<script>
import Header from'@/components/layout/Header'
import Footer from'@/components/layout/Footer'

import vueCanvasNest from 'vue-canvas-nest'


export default {
  name: 'App',
  components: {
    Header,
    Footer,
    vueCanvasNest
  },
  mounted(){
		
  }
}
</script>

<style lang="scss">
	$fa-font-path: "~font-awesome/fonts/";
	@import "~font-awesome/scss/font-awesome";
	
	*{margin: 0;padding: 0;box-sizing: border-box;}
	html,body{height: 100%;font-family:"Helvetica Neue", NotoSansHans-Regular,AvenirNext-Regular,arial,Hiragino Sans GB,"Microsoft Yahei","Hiragino Sans GB","WenQuanYi Micro Hei",sans-serif;}
	a{text-decoration: none;color: #000;}
	ul,li{list-style: none;}
	em,i{font-style: normal;}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
.mainwrap{width: 1200px;margin: 0 auto;}
.clr:after {display: block;content: " ";clear: both;height: 0;}
.clr {zoom: 1;}
.fl{float: left;}
.fr{float: right;}
.title-popover{background: #fff;padding: 10px;border-radius: 5px;margin-top: -10px;font-size: 14px;
	.arrow{content: '';position: absolute;bottom: -10px;left: 50%;margin-left: -10px;width: 0;height: 0;border-left: 10px solid transparent;border-right: 10px solid transparent;border-top: 10px solid #fff;z-index: 999;}
}
</style>
