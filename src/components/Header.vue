<template>
	<div class="header">
		<div class="navs mainwrap">
			<div class="topleft">
				<img src="../assets/logo.png">
				<div class="toptxt">Vue.js</div>
				<div class="arrowdown">
					<i></i>
				</div>
				<div class="topmenu">
					
				</div>
			</div>
		</div>
		
	</div>
</template>

<script>
	export default{
		name:'Header'
	}
</script>

<style scoped lang="scss">
	.header{border-top:4px solid #4fc08d;height:auto;height:54px;box-shadow: 0 0 10px 0 rgba(42,42,42,0.1);
		.navs{height:50px;
			.topleft{float: left;display: flex;height: 100%;align-items: center;cursor: pointer;
				img{width: 26px;height: 26px;margin-right: 10px;}
				.toptxt{float: right;color: #888;font-size: 14px;font-weight: bold;}
				.arrowdown{margin-left: 15px;
					i{display: inline-block;width: 0; height: 0;border-left: 5px solid transparent;border-right: 5px solid transparent;border-top: 6px solid #666;}
				}
				.topmenu{overflow-x: hidden;overflow-y: auto;
					
				}
			}
		}
		
	}
</style>