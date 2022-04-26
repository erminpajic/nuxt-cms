<template>
	<div :class="['tab', {'active': isActive}]">
		<slot/>
	</div>
</template>

<style>
.tab{display: none;}
.tab.active{display: block;}
</style>

<script>
export default {
	props: {
		title: {
			type: String,
			default: 'Tab'
		}
	},
	data() {
		return {
			isActive: 0
		}
	}
}
</script>