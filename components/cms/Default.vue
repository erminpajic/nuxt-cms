<template>
	<div class="main wrapper clear">
		<div class="main-content">
			<UiBreadcrumbs :breadcrumb="data"/>
			<h1>{{ data.seo_h1 }}</h1>
			<div v-html="data.content" v-interpolation></div>
		</div>

		<aside class="sidebar">
			<UiSidebarNav/>
		</aside>
	</div>
</template>

<script>
	export default {
		props: ['data']
	}
</script>