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
	$container-large-desktop: 1200px;
	$btn-primary-bg: #00b5ad;
	$btn-primary-border: #00b5ad;
	$label-primary-bg: #00b5ad;
	$pagination-active-bg: #00b5ad;
	$pagination-active-border: #00b5ad;
	$pagination-color: #00b5ad;
	$input-border-focus: #00b5ad;
	$link-color: #12c4c5;
	$link-hover-color: #22ddde;
	$icon-font-path: "~bootstrap-sass/assets/fonts/bootstrap/";
	$fa-font-path: "~font-awesome/fonts/";
	@import "~font-awesome/scss/font-awesome";
	@import "~bootstrap-sass/assets/stylesheets/_bootstrap";
	@import "./styles/main";
	
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
  min-height: 100%;
  height: auto;
  position: relative;
}
.mainwrap{width: 1200px;margin: 0 auto;}
.clr:after {display: block;content: " ";clear: both;height: 0;}
.clr {zoom: 1;}
.fl{float: left;}
.fr{float: right;}
.title-popover{background: #fff;padding: 10px;border-radius: 5px;margin-top: -10px;font-size: 14px;
	.arrow{content: '';position: absolute;bottom: -10px;left: 50%;margin-left: -10px;width: 0;height: 0;border-left: 10px solid transparent;border-right: 10px solid transparent;border-top: 10px solid #fff;z-index: 999;}
}
.container{height: 100%;width: 1200px;margin: 0 auto;padding-bottom: 340px;margin-top: 20px;min-height: 100%;}
</style>
