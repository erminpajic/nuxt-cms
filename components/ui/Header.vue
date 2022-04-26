<template>
	<div>
		<header class="header">
			<div class="top">
				<div class="wrapper clear">
					<ul class="nav nav-left">
						<NuxtLink custom v-slot="{href, navigate, /*isActive,*/ isExactActive}" v-for="item in menuItems" :key="item.id" :to="item.url">
							<li :class="[{'selected': isExactActive}]">
								<a v-if="item.url.startsWith('http')" :href="item.url" target="_blank"><span>{{item.title}}</span></a>
								<a v-else :href="href" @click="navigate">
									<span>{{ item.title }}</span>
								</a>
							</li>
						</NuxtLink>
					</ul>
					<ul class="nav nav-right">
						<li><a href="https://b2b.cotra.hr/korisnik/"><span>Moj račun</span></a></li>
						<li><a href="https://b2b.cotra.hr/korisnik/my_webshoporder/"><span>Moje narudžbe</span></a></li>
						<li><a href="https://b2b.cotra.hr/korisnik/edit/"><span>Uredi podatke</span></a></li>
						<li><a href="https://b2b.cotra.hr/korisnik/change_password/"><span>Promjeni lozinku</span></a></li>
						<li><a href="https://b2b.cotra.hr/korisnik/logout/?redirect=%2Fo-nama%2F"><span>Odjava</span></a></li>
					</ul>
				</div>
			</div>
			<div class="wrapper header-main">
				<NuxtLink to="/" class="logo"/>
				<div class="after-logo"></div>

				<UiSearchForm/>

				<div class="fz0 header-container">	
					<!-- FIXME if (!Arr::get($info, 'user_disabled_order')):  -->
					<a class="btn btn-quickorder" href="#"><span>{{ cmslabel('quick_order', 'title') }}</span></a>

					<WebshopWidgetShoppingCart/>

					<a class="btn-toggle-nav mobile animated-icon-container">
						<div class="animated-icon">
							<span></span>
							<span></span>
							<span></span>
							<span></span>
						</div>
					</a>	
				</div>
			</div>
			<div class="mobile-menu-cnt mobile"></div>
		</header>
		<div class="header-placeholder"></div>

		<div class="subheader">
			<div class="wrapper fz0">
				<div class="categories-cnt">
					<a class="btn btn-toggle-categories" href="/">{{ cmslabel('product_categories', 'title') }}</a>
					<ul class="categories">
						<li class="has-children"><a href="#">Lorem, ipsum dolor</a>
							<div class="subcategories-cnt fz0">
								<ul class="subcategories">
									<li class="has-children">
										<a href="/">INSTALACIJSKI KABELI I VODIČI</a>
										<div class="subsubcategories-cnt">
											<ul class="subsubcategories">
												<li><a href="#">NYM / YM (PP-Y)</a></li>
											</ul>
										</div>
									</li>
								</ul>
							</div>
						</li>
						<li><a href="#">Lorem, ipsum dolor</a></li>
						<li><a href="#">Lorem, ipsum dolor</a></li>
						<li><a href="#">Lorem, ipsum dolor</a></li>
						<li><a href="#">Lorem, ipsum dolor</a></li>
						<li><a href="#">Lorem, ipsum dolor</a></li>
						<li><a href="#">Lorem, ipsum dolor</a></li>
						<li><a href="#">Lorem, ipsum dolor</a></li>
						<li><a href="#">Lorem, ipsum dolor</a></li>
						<li><a href="#">Lorem, ipsum dolor</a></li>
						<li><a href="#">Lorem, ipsum dolor</a></li>
					</ul>
					<div class="menu-slider-cnt">
						<HeroSlider/>
					</div>
				</div>

				<NewsTicker/>
			</div>
		</div>
	</div>
</template>

<script>
import HeroSlider from '../ui/HeroSlider.vue'
import NewsTicker from '../ui/NewsTicker.vue'
export default {
	computed: {
		menuItems() {
			return this.$store.getters["cms/getMenu"]("headless-main-menu");
		}
	},
	components: {
		HeroSlider,
		NewsTicker
	}
}
</script>

<style lang="less">
.header{position: relative; z-index: 101;}
.top{border-bottom: 1px solid @gray; font-weight: 500; height: 35px; line-height: 35px;}
.logo{position: absolute; display: block; z-index: 99; width: 130px; height: 50px; background:url(~assets/images/logo.png) no-repeat left top; background-size: contain; position: absolute; top: 22px; left: 0;}
.after-logo{width: 117px; height: 29px; background: url(~assets/images/sve-za-struju.svg) top left; background-size: contain; position: absolute;left: 160px; top: 26px; background-repeat:no-repeat;}
.header-main{height: 80px; z-index: 100;}
.header-container{position: absolute; right: 0; top: 15px;}
.btn-quickorder{
	height: 50px; line-height: 51px; font-size: 15px; font-weight: 500; padding: 0; min-width: 200px; text-align: center;
	span{
		position: relative; padding-left: 37px;
		&:before{.icon-menu; font: 20px/20px @fonti; position: absolute; left: 0; top: -1px; color: #fff;}	
	}
} 
.header-placeholder{display: none;}
.btn-toggle-categories{
	width: 304px; padding: 0 20px; background: @primaryColor; position: relative; font-size: 16px; font-weight: 500; text-align: left;
	&:before{position: absolute; .icon-arrow; font: 10px/10px @fonti; color: #fff; right: 20px; top: 21px; .rotate(-90deg);}
}

@media screen and (max-width: 1300px) {
		/*------- 1300 header -------*/
	.top{height: 31px; line-height: 31px;}
	.nav{
		a{font-size: 12px; padding: 0 10px;}
	}
	.logo{width: 150px; height: 27px; top: 30px;}
	.after-logo{width: 95px; height: 23px; left: 83px; top: 33px;}
}
	/*------- /1300 header -------*/

	/*------- 990 header -------*/

@media screen and (max-width: 990px) {
	.top, .btn-quickorder{display: none;}
	.logo{width: 240px; height: 47px; top: 20px; left: 20px;}
	.after-logo{width: 100px; height: 27px; left: 160px; top: 33px}
	.header-main{height: 87px;}
	.header-container{right: 20px; top: 20px;}
	.mobile-menu-cnt{position: absolute; left: 0; right: 0; top: 87px; display: block; background: #fff; z-index: 200; display: none;
		.btn-quickorder, .categories{display: block;}
		&.active{display: block;}
	}
	.btn-quickorder{
		text-align: left; background: #fff!important; color: @black!important; border-bottom: 1px solid #E8E8E8; border-top: 1px solid #E8E8E8; padding: 0 25px; font-size: 16px; font-weight: bold;
		span{
			padding: 0;
			&:before{display: none;}
		}
	}
}
	/*------- /990 header -------*/

	/*------- 750 header -------*/
	
@media screen and (max-width: 750px) {
	.header-main{height: 44px; border-bottom: 1px solid #e8e8e8; position: relative; left: 0; right: 0;}
	.logo{width: 185px; top: 7px; left: 7px; height: 34px;}
	.after-logo{width: 80px; height: 20px; left: 100px; top: 15px;}
	.header-container{right: 0; top: 0;}
	.btn-toggle-nav{width: 40px; height: 43px; border-radius: 0; background: #fff; margin-left: 0; border-left: 1px solid #E8E8E8;}
	.animated-icon{
		width: 16px; height: 12px; left: 12px;
		span{background: @primaryColor; height: 2px;}
	}
	.animated-icon span:nth-child(2), .animated-icon span:nth-child(3){top: 5px;}
	.animated-icon span:nth-child(4){top: 10px;}
	.btn-quickorder{padding: 0 15px;}
	.header-placeholder{height: 44px; display: block;}
	.header{position: fixed; left: 0; right: 0; background: white;z-index: 700;}
}
	/*------- /750 header -------*/		
</style>