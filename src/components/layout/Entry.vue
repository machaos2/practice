<template>
	<div class="navRight fr">
		<div class="navs">
			<a href="#" class="userbtn">
				<i class="fa fa-user"></i> 登陆
			</a>
			<router-link to="/auth/register" class="userbtn">
				<i class="fa fa-user-plus"></i> 注册
			</router-link>
		</div>
	</div>
</template>

<script>
	export default {
	  name: 'Entry'
	}
</script>

<style lang="scss">
	.navRight{
		.navs{
			.userbtn{display: inline-block;font-size: 14px;padding: 5px 12px;border: 1px solid #ccc;user-select: none;margin-top: 8px;
				&:hover{background: #eee;}
			}
		}
	}
</style>