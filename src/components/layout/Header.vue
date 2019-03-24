<template>
	<div class="header">
		<div class="navs mainwrap">
			<div class="topleft" @click="dropDown">
				<img src="../../assets/logo.png">
				<div class="toptxt">Vue.js</div>
				<div class="arrowdown">
					<i></i>
				</div>
				<div class="topmenu" v-show="dd === true">
					<a href="/" v-for="title in titles"><img :src="title.src"/>{{title.name}}</a>
				</div>
			</div>
			
			<div class="topList clr">
				<ul class="clr">
					<li v-for="(item,index) in items" :class="{ active : index === activList}">
						<a href="#" @click="changeBg(index)">{{item}}</a>
					</li>
				</ul>
			</div>
			
			<div class="navRight">
				<Entry/>
			</div>
		</div>
		
		
		
	</div>
</template>

<script>
	import Entry from'@/components/layout/Entry'
	export default{
		name:'Header',
		components:{
			Entry
		},
		data(){
			return{
				dd:false,
				titles:[
					{
						name:'Vue.js',
						src:'http://www.hfyjy.com/images/vue/vue.png'
					},
					{
						name:'PHP',
						src:'http://www.hfyjy.com/images/vue/La.png'
					},
					{
						name:'Vue.js',
						src:'http://www.hfyjy.com/images/vue/vue.png'
					},
					{
						name:'PHP',
						src:'http://www.hfyjy.com/images/vue/La.png'
					}
				],
				items:['社区', '头条', '问答', '教程'],
				activList:0
			}
		},
		methods:{
			dropDown(){
				this.dd = !this.dd;
			},
			changeBg(index){
				this.activList = index;
			}
		}
	}
</script>

<style scoped lang="scss">
	.header{border-top:4px solid #4fc08d;height:auto;height:54px;box-shadow: 0 0 10px 0 rgba(42,42,42,0.1);background: #fff;
		.navs{height:50px;font-size:14px;
			.topleft{float: left;display: flex;height: 100%;align-items: center;cursor: pointer;
				img{width: 26px;height: 26px;margin-right: 10px;}
				.toptxt{float: right;color: #888;font-size: 14px;font-weight: bold;}
				.arrowdown{margin-left: 15px;
					i{display: inline-block;width: 0; height: 0;border-left: 5px solid transparent;border-right: 5px solid transparent;border-top: 6px solid #666;}
				}
				.topmenu{position: absolute;top: 56px;box-shadow: 0 2px 3px 0 rgba(34,36,38,.15);font-size: 14px;text-align: left;margin-top: 2px;
					>a{align-items: center;padding:10px 16px;padding-right: calc(1.14285714rem + 17px);display: block;height: 100%;line-height: 24px;color: #777;
						img{width: 20px;height: 20px;margin-right: 10px;margin-bottom: -5px;}
						&:hover{background: #eee;}
					}
				}
			}
			.topList{float: left;
				ul{float:left;height: 50px;margin-left: 10px;
					li{float: left;
						a{padding: 15px 15px 9px;display: block;height: 50px;}
						
					}
				}
			}
			.navRight{float: right;}
		}
		
	}
	.active{background: rgba(0,0,0,0.03);}
</style>