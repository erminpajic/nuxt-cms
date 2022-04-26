<template>
	<div class="tabs-container">
		<ul class="tabs">
			<li 
				v-for="(tab, index) in tabs" :key="index"
				@click="selectTab(index)"
				:class="{'active': selectedTab == index}"
			><span>{{ tab.title }}</span></li>
		</ul>
		<div class="tabs-content">
			<slot/>
		</div>
	</div>
</template>

<style lang="less" scoped>
.tabs{
	font-size: 0; text-align: center; white-space: nowrap; position: absolute; top: -60px; left: 0; right: 0; color: #fff;
	li{
		display: inline-block; vertical-align: top; cursor: default; background: @primaryColor; font-size: 18px; height: 60px; line-height: 61px; width: 200px; font-weight: 500; .transition(all);
		&.active{background: #fff; color: @red;}
	}
}
.tabs-content{padding: 30px 0 90px;}
</style>

<script>
export default {
	data() {
		return {
			tabs: [],
			selectedTab: 0
		}
	},
	mounted() {
		this.tabs = this.$children;
		this.selectTab(0);
	},
	methods: {
		selectTab(i) {
			this.selectedTab = i

			this.tabs.forEach((tab, index) => {
				tab.isActive = (index === i)
			})
		}
	}
}
</script>