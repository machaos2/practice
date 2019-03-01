<template>
	<div class="footer">
		<div class="fcenter">
			<div class="fcTop clr">
				<div class="fore">
					<h4>关于 LearnKu</h4>
					<div class="fcontent">LearnKu.com 是一个开发者知识社区，这里不仅有高品质的编程知识，还有热情友善、乐于分享的同学。</div>
				</div>
				<div class="fore">
					<h4>关于 LearnKu</h4>
					<div class="fcontent">LearnKu.com 是一个开发者知识社区，这里不仅有高品质的编程知识，还有热情友善、乐于分享的同学。</div>
				</div>
				<div class="fore">
					<h4>关于 LearnKu</h4>
					<div class="fcontent">LearnKu.com 是一个开发者知识社区，这里不仅有高品质的编程知识，还有热情友善、乐于分享的同学。</div>
				</div>
				<div class="fore">
					<h4>关于 LearnKu</h4>
					<div class="fcontent">LearnKu.com 是一个开发者知识社区，这里不仅有高品质的编程知识，还有热情友善、乐于分享的同学。</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	export default{
		name:'Footer',
		data(){
			return{
				
			}
		}
	}
</script>

<style scoped lang="scss">
	.footer{position: absolute;bottom: 0;padding: 40px 0;background: #1b1c1d;width: 100%;
		.fcenter{width: 1200px;margin: 0 auto;
			.fcTop{
				.fore{width: 25%;float: left;}
				.fore~.fore{border-left: 1px solid #fff;}
			}
		}
	}
</style>