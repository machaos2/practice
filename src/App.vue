<template>
  <div id="app">
  	<Header/>
  </div>
</template>

<script>
import Header from'./components/Header'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style>
	*{margin: 0;padding: 0;box-sizing: border-box;}
	html,body{font-family:"Helvetica Neue", NotoSansHans-Regular,AvenirNext-Regular,arial,Hiragino Sans GB,"Microsoft Yahei","Hiragino Sans GB","WenQuanYi Micro Hei",sans-serif;}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.mainwrap{width: 1200px;margin: 0 auto;}
.clr:after {display: block;content: " ";clear: both;height: 0;}
.clr {zoom: 1;}
</style>
