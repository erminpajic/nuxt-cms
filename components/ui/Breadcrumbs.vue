<template>
	<!-- FIXME PROG dobivanje breadcrumbs podataka kroz api -->
	<ul class="bc">
		<li><NuxtLink to="/">Početna</NuxtLink></li>
		<li><NuxtLink :to="breadcrumb.slug">{{ breadcrumb.title }}</NuxtLink></li>
	</ul>
</template>

<style lang="less" scoped>
.bc{
	padding: 25px 0 17px; font-size: 13px; list-style: none; color: #74767A; line-height: 15px; display: flex; flex-wrap: wrap;
	li:last-child>a{text-decoration: none; pointer-events: none; color: #74767A; margin: 0; padding: 0;}
	li:not(:last-child) a:after{.icon-arrow; font: 7px/7px @fonti; color: @primaryColor; position: absolute; right: 0; top: 5px; .rotate(180deg);}
	a{text-decoration: underline; padding: 0 14px 0 0; margin: 0 8px 0 0; position: relative; color: @primaryColor;}
}

@media (max-width: @t){
	.bc{text-align: center;}
}

@media (max-width: @m){
	.bc{
		text-align: left; padding: 15px 0 10px;
		a, span{font-size: 10px;}
		a:after{font-size: 6px; line-height: 6px;}
	}	
}
</style>

<script>
export default {
	props: ['breadcrumb']
}
</script>