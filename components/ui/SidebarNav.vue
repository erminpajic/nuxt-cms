<template>
	<ul class="nav-sidebar">
		<NuxtLink custom v-slot="{href, navigate, /*isActive,*/ isExactActive}" v-for="menuItem in sidebarMenu" :key="menuItem.id" :to="menuItem.url">
			<li :class="{'selected': isExactActive}">
				<a :href="href" @click="navigate">{{ menuItem.title }}</a>
			</li>
		</NuxtLink>
	</ul>
</template>

<style lang="less">
.nav-sidebar{
	list-style: none; font-weight: 500; border-top: 1px solid @gray; 
	li{border-bottom: 1px solid @gray;}
	li.selected, li:hover{
		a{color: #B0B0AF;}
	}
	a{display: block; padding: 12px 20px 12px; font-size: 16px; line-height: 20px; color: @primaryColor;}
}
</style>

<script>
export default {
	computed: {
		sidebarMenu() {
			return this.$store.getters['cms/getMenu']('sidebar-menu')
		}
	}
}
</script>