<template>
	<div>
		<BrandsSlider/>
		<SpecialProducts/>
		<LatestOrders/>
	</div>
</template>

<style lang="less">
	@media screen and (min-width: 1680px) {
		.page-homepage{
			.categories, .menu-slider-cnt{display: block;}
			.subheader{margin-bottom: 560px;}
			.btn-toggle-categories{background: @secondaryColor;
				&:before{display: none; .icon-x; font: 10px/10px @fonti; color: #fff; right: 17px; top: 21px;}
				&:hover{background: @black;}
			}
		}
	}
</style>

<script>
import BrandsSlider from '../ui/Brands.vue'
import SpecialProducts from '../ui/SpecialProducts.vue'
import LatestOrders from '../webshop/widget/LatestOrders.vue'
export default {
	props: ['data'],
	components: {
		BrandsSlider,
		SpecialProducts,
		LatestOrders
	}
}
</script>