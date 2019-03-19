<template>
	<div class="footer">
		<div class="fcenter">
			<div class="fcTop clr">
				<div class="fore">
					<h4>关于 LearnKu</h4>
					<div class="fcontent">LearnKu 是专为终身学习者定制的编程知识社区。</div>
				</div>
				<div class="fore">
					<h4>资源推荐</h4>
					<div class="fcontent">暂无内容~~</div>
				</div>
				<div class="fore">
					<h4>赞助商</h4>
					<div class="fcontent">
						<ul class="sponsors">
							<li v-for="spon in sponsor" v-title="spon.title" class="miniTxt">
								<a :href="spon.linkto">
									<img :src="spon.logo"/>
								</a>
							</li>
						</ul>
					</div>
				</div>
				<div class="fore">
					<h4>其他信息</h4>
					<div class="fcontent">
						<ul class="other">
							<li v-for="oth in others">
								<a :href="oth.linkto"><i class="simg1"></i>{{oth.content}}</a>
							</li>
						</ul>
					</div>
				</div>
			</div>
			<div class="fotLine"></div>
			<div class="authorBy">
				<p>由 Pluto 设计和编码 <em>❤</em></p>
			</div>
		</div>
	</div>
</template>

<script>
	import title from '@/directives/title'
	export default{
		name:'Footer',
		directives:{
			title
		},
		data(){
			return{
				sponsor:[
					{
						logo:"http://www.hfyjy.com/images/sponsor/sponsor1.png",
						title:"由Ucloud赞助",
						linkto:"#"
					},
					{
						logo:"http://www.hfyjy.com/images/sponsor/sponsor2.png",
						title:"由又拍云赞助",
						linkto:"#"
					},
					{
						logo:"http://www.hfyjy.com/images/sponsor/sponsor3.png",
						title:"由sendcloud赞助",
						linkto:"#"
					}
				],
				others:[
					{
						content:"软件外包",
						linkto:"#"
					},
					{
						content:"商务合作",
						linkto:"#"
					},
					{
						content:"联系站长",
						linkto:"#"
					},
					{
						content:"PHP / Laravel 月刊",
						linkto:"#"
					}
				]
			}
		}
	}
</script>

<style scoped lang="scss">
	.footer{position: absolute;bottom: 0;padding: 40px 0;background: #1b1c1d;width: 100%;
		.fcenter{width: 1200px;margin: 0 auto;
			.fcTop{display: flex;
				.fore{padding: 1rem;flex: 1;color: #fff;
					h4{margin-bottom: 10px;font-size: 15px;}
					.fcontent{font-size: 14px;padding-top: 5px;
						.sponsors{
							li{display: list-item;margin-top: 5px;
								a{line-height: 28px;
									img{height: 20px;}
								}
							}
						}
						.other{
							li{
								a{color: hsla(0,0%,100%,.5);
								}
							}
						}
					}
				}
				.fore~.fore{border-left: 1px solid rgba(211,224,233,.15);
					.fcontent{color: #a5a5a5;}
				}
			}
			.fotLine{margin: 28px 0;border-bottom: 1px solid rgba(211,224,233,.15);}
			.authorBy{
				p{font-size: 14px;color: rgb(137, 137, 140);
					em{color: #e27575;}
				}
			}
		}
	}
</style>