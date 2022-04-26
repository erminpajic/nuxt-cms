<template>
	<div class="ww cart" data-active-cart>
		<NuxtLink to="/webshop/" class="ww-items">
			<span>Košarica<span class="value w-total-items"><ShoppingCartCounter/></span></span>
		</NuxtLink>

		<!-- Min order alert -->
		<span class="cart_info_total_items_base" style="position: absolute; top: -500px;">0</span>
	</div>
</template>

<script>
import ShoppingCartCounter from "./ShoppingCartCounter.vue";
export default {
	components: { ShoppingCartCounter }
}
</script>

<style lang="less">
.ww{
	display: inline-block; vertical-align: top; margin-left: 15px; position: relative;
	&.active-cart{
		.w-total-items{display: block;}
		.ww-items{
			background: @green;
			&:hover{text-decoration: none; background: @green/1.1;}
		}
	}
	&:hover .ww-preview{display: block;}
}
.ww-items{
	display: block; height: 50px; background: @green; font-weight: 500; min-width: 200px; text-align: center; line-height: 50px; color: #fff!important; text-decoration: none; font-size: 15px; border-radius: @borderRadius; .transition(all);
	&>span{
		position: relative; padding-left: 40px;
		&:before{.icon-cart; font: 23px/22px @fonti; position: absolute; left: 0; top: -2px;}
	}
	&:hover{text-decoration: none; background: @green/1.1;}
}
.w-total-items{font-size: 14px; font-weight: bold; position: absolute; left: 25px; top: -9px; line-height: 16px; display: none;}

.active-cart{
	.w-total-items{display: block;}
}

@media (max-width: @t){
	.ww-items{width: 47px; min-width: 0; height: 47px; font-size: 0; line-height: 47px;}
	.ww-items>span{
		display: block; padding: 0;
		&:before{font-size: 20px; line-height: 20px; left: 11px; top: 15px;}
	}
	.w-total-items{font-size: 12px; left: 32px; top: 8px;}	
}

@media (max-width: @tp){
	.ww{margin-left: 0;}
	.ww-items{
		width: 40px; height: 43px; line-height: 44px; background: #fff!important; border-left: 1px solid #E8E8E8; color: @black!important;
		&>span{
			&:before{color: @black; font-size: 16px; line-height: 16px;}
		}
	}
	.w-total-items{font-size: 10px; left: 28px;}	
}
</style>