<template>
	<div class="news-ticker">
		<div class="splide__track">
			<div class="splide__list">
				<div class="splide__slide news-ticker-item" v-for="slide in slider" :key="slide.id">
					<NuxtLink :to="slide.link">{{ slide.title }}</NuxtLink>
				</div>
			</div>
		</div>
	</div>
</template>

<style lang="less">
.news-ticker{
	font-size: 0; overflow: hidden; padding: 15px 20px; display: inline-block; vertical-align: top; width: 1376px; border: 1px solid @gray;
	@media (max-width: @l){width: calc(~"100% - 304px");}
	@media (max-width: @t){width: calc(~"100% - 224px");}
	@media (max-width: @tp){width: 100%; border-left: 0; border-right: 0;}
	@media (max-width: @m){padding: 5px 0; border-top: 0;}
}
.news-ticker-item{ 
	float: left; position: relative; font-size: 14px; line-height: 18px; padding: 0 0 0 27px; margin: 0 0 0 20px; white-space: nowrap;
    @media (max-width: @t){font-size: 12px;}
	@media (max-width: @m){padding-left: 21px; margin-left: 16px;}
	&:before{
		.pseudo(7px,7px); background: @secondaryColor; border-radius: 100%; left: 0; top: 6px;
		@media (max-width: @m){top: 7px;}
	}
	&:first-child{
		padding: 0;
		&:before{display: none;}
	}
	a{text-decoration: underline; color: #000;}
	&:hover{
		a{color: @secondaryColor;}
	}
}
</style>

<script>
import Splide from '@splidejs/splide';
import { AutoScroll } from '@splidejs/splide-extension-auto-scroll';
export default {
	computed: {
		slider() {
			const items = this.$store.getters['cms/getRotator']('news');
			return items;
		}
	},
	mounted() {
		new Splide('.news-ticker', {
			type: 'loop',
			focus: 'center',
			perPage: 10,
			autoWidth: true,
			pagination: false,
			arrows: false,
			autoScroll: {
				speed: 0.6
			}
		}).mount({AutoScroll});
	}
}
</script>