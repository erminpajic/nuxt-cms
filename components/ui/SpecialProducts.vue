<template>
	<div class="cw-cnt">
		<div class="cw">
			<div class="wrapper">
				<Tabs class="cw-tabs-container">
					<Tab :title="cmslabel('on_sale', 'title')">
						<div class="c-items cw-items fz0">
							<CatalogItem/>
							<CatalogItem/>
							<CatalogItem/>
							<CatalogItem/>
							<CatalogItem/>
							<CatalogItem/>
						</div>
						<div class="cw-all-products-cnt">
							<a class="btn cw-all-products" href="/">{{ cmslabel('show_all', 'title') }}</a>
						</div>
					</Tab>
					<Tab :title="cmslabel('new', 'title')">
						<div class="c-items cw-items fz0">
							<CatalogItem/>
							<CatalogItem/>
							<CatalogItem/>
							<CatalogItem/>
							<CatalogItem/>
						</div>
						<div class="cw-all-products-cnt">
							<a class="btn cw-all-products" href="/">{{ cmslabel('show_all', 'title') }}</a>
						</div>
					</Tab>
				</Tabs>
			</div>
		</div>
	</div>	
</template>

<style lang="less">

</style>

<script>
import Tabs from './Tabs.vue'
import Tab from './Tab.vue'
import CatalogItem from '../catalog/IndexEntry.vue'
export default {
	components: {
		Tabs,
		Tab,
		CatalogItem
	}
}
</script>