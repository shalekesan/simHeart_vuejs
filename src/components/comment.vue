<template>
	<div id="disqus_thread" v-show-comment="post_info"></div>
</template>
<script>
	module.exports = {
		props:['post_info']
	}
</script>