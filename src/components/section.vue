<style>
	section{
		padding:40px 18% 0;
	}
	section h2{
		text-align:center;
		padding:0 20px;
	}
	section a,section article{
		word-wrap: break-word;
		word-break: break-all;
	}
	.division{
		text-align: center;
		border-bottom:1px dotted #ccc;
		padding-bottom:20px;
	}
	.cover img{
		-webkit-border-radius: .5em;
		-moz-border-radius: .5em;
		border-radius: .5em;
		max-width:100%;
		margin:0 auto;
		margin-bottom:20px;
	}
</style>
<template>
	<template v-for="post in posts">
		<section>
			<h2><a v-link="{name:'post',params:{id:post.id}}">{{ post.title }}</a></h2>
			<template v-if="post.image">
				<div class="cover">
					<img :src="post.image">
				</div>
			</template>
			<article>
				{{ post.meta_description }}
			</article>
			<p class="division"><a v-link="{name:'post',params:{id:post.id}}">--阅读全文--</a></p>
		</section>
	</template>
</template>

<script>
	module.exports = {
		props:['posts']
	}
</script>
