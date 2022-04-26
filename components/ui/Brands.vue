<template>
	<div class="brands">
		<div class="wrapper">
			<div class="brands-items">
				<div class="brands-items-col brands-items-col1">
					<div class="brands-slider">
						<div class="splide__track">
							<div class="splide__list">
								<div class="splide__slide">
									<a href="/" class="brand-item">
										<img src="https://b2b.cotra.hr/upload/catalog/manufacturer/thumb/lovato-kon-ar_609a7acd803db_180x80r.png" width="90" height="40" alt="">
									</a>
								</div>
								<div class="splide__slide">
									<a href="/" class="brand-item">
										<img src="https://b2b.cotra.hr/upload/catalog/manufacturer/thumb/lovato-kon-ar_609a7acd803db_180x80r.png" width="90" height="40" alt="">
									</a>
								</div>
								<div class="splide__slide">
									<a href="/" class="brand-item">
										<img src="https://b2b.cotra.hr/upload/catalog/manufacturer/thumb/lovato-kon-ar_609a7acd803db_180x80r.png" width="90" height="40" alt="">
									</a>
								</div>
								<div class="splide__slide">
									<a href="/" class="brand-item">
										<img src="https://b2b.cotra.hr/upload/catalog/manufacturer/thumb/lovato-kon-ar_609a7acd803db_180x80r.png" width="90" height="40" alt="">
									</a>
								</div>
								<div class="splide__slide">
									<a href="/" class="brand-item">
										<img src="https://b2b.cotra.hr/upload/catalog/manufacturer/thumb/lovato-kon-ar_609a7acd803db_180x80r.png" width="90" height="40" alt="">
									</a>
								</div>
								<div class="splide__slide">
									<a href="/" class="brand-item">
										<img src="https://b2b.cotra.hr/upload/catalog/manufacturer/thumb/lovato-kon-ar_609a7acd803db_180x80r.png" width="90" height="40" alt="">
									</a>
								</div>
								<div class="splide__slide">
									<a href="/" class="brand-item">
										<img src="https://b2b.cotra.hr/upload/catalog/manufacturer/thumb/lovato-kon-ar_609a7acd803db_180x80r.png" width="90" height="40" alt="">
									</a>
								</div>
								<div class="splide__slide">
									<a href="/" class="brand-item">
										<img src="https://b2b.cotra.hr/upload/catalog/manufacturer/thumb/lovato-kon-ar_609a7acd803db_180x80r.png" width="90" height="40" alt="">
									</a>
								</div>
								<div class="splide__slide">
									<a href="/" class="brand-item">
										<img src="https://b2b.cotra.hr/upload/catalog/manufacturer/thumb/lovato-kon-ar_609a7acd803db_180x80r.png" width="90" height="40" alt="">
									</a>
								</div>
								<div class="splide__slide">
									<a href="/" class="brand-item">
										<img src="https://b2b.cotra.hr/upload/catalog/manufacturer/thumb/lovato-kon-ar_609a7acd803db_180x80r.png" width="90" height="40" alt="">
									</a>
								</div>
								<div class="splide__slide">
									<a href="/" class="brand-item">
										<img src="https://b2b.cotra.hr/upload/catalog/manufacturer/thumb/lovato-kon-ar_609a7acd803db_180x80r.png" width="90" height="40" alt="">
									</a>
								</div>
								<div class="splide__slide">
									<a href="/" class="brand-item">
										<img src="https://b2b.cotra.hr/upload/catalog/manufacturer/thumb/lovato-kon-ar_609a7acd803db_180x80r.png" width="90" height="40" alt="">
									</a>
								</div>																									
							</div>
						</div>
					</div>
				</div>
				<div class="brands-items-col brands-items-col2">
					<a class="btn-all-brands" href="/">{{ cmslabel('all_brands', 'title') }}</a>
				</div>
			</div>
		</div>
	</div>
</template>

<style lang="less">
.brands{
	font-size: 14px; text-align: center; padding: 20px 0;
	@media (max-width: @t){padding: 12px 0 40px;}
	@media (max-width: @tp){padding: 12px 20px 25px;}
	@media (max-width: @m){padding: 20px 15px 15px;}
	img{
		max-width: 100%; width: auto; height: auto; display: inline-block; vertical-align: middle;
		@media (max-width: @l){padding: 0 14px;}
		@media (max-width: @t){padding: 0 30px;}
		@media (max-width: @tp){padding: 0 15px;}
		@media (max-width: @m){padding: 0 5px; max-height: 25px;}
	}
}
.brands-items{
	display: flex; align-items: center;
	@media (max-width: @t){flex-wrap: wrap;}
}
.brands-items-col1{
	width: calc(~"100% - 250px"); flex-grow: 0; flex-shrink: 0;
	@media (max-width: @m){width: 100%; margin-bottom: 20px;}
}
.brands-items-col2{flex-grow: 1;}
.brand-item{
	flex-grow: 1; display: block; text-align: center; justify-content: center; align-items: center; text-decoration: none; height: 82px; line-height: 82px; font-size: 14px; text-transform: uppercase; color: @textColor;
	@media (max-width: @t){width: 14%; height: 70px; line-height: 70px;}
	@media (max-width: @m){width: 100%; display: inline-block; vertical-align: middle; height: 30px; line-height: 30px;}
	img{
		max-height: 50px; width: auto;
		@media (max-width: @m){max-width: 95%; height: auto;}
	}
}
.btn-all-brands{ 
	background: @primaryColor; text-decoration: none; color: white; font-size: 16px; margin-left: 30px;; font-weight: 500; width: calc(~"100% - 30px"); height: 50px; line-height: 50px; border: 1px solid #e0e7f1; text-align: center; display: inline-block; vertical-align: middle; .transition(all);
	@media (max-width: @tp){height: 40px; line-height: 40px; font-size: 14px;}
	@media (max-width: @m){background: @black; color: #fff; border: 0; border-radius: 2px; height: 36px; line-height: 38px; width: 100%; margin: 0;}
	&:hover{color: white; }
}
@media (max-width: @m){
		.owl-nav{left: -27px; right: -27px; top: 0; margin: 0;}
		.owl-prev, .owl-next{
			background: transparent;
			&:before{color: @black;}
		}
}
</style>

<script>
import Splide from '@splidejs/splide';
export default {
	mounted() {
		new Splide('.brands-slider', {
			perPage: 7,
			arrows: false,
			pagination: false,
			//autoplay: true,
			rewind:  true,
			speed: 1000,
			rewindSpeed: 1000
		}).mount();	
	}
}
</script>