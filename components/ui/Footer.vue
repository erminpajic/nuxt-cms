<template>
	<footer class="footer">
		<div class="wrapper">
			<div class="footer-row footer-row1">
				<div class="footer-col footer-col1">
					<div class="footer-title">{{ cmslabel('footer_team', 'title') }}</div>
					<ul class="footer-nav">
						<NuxtLink custom v-slot="{href, navigate, /*isActive,*/ isExactActive}" v-for="menuItem in footerCol1Menu" :key="menuItem.id" :to="menuItem.url">
							<li :class="{'selected': isExactActive}">
								<a :href="href" @click="navigate">{{ menuItem.title }}</a>
							</li>
						</NuxtLink>
					</ul>
					<div class="footer-logo"></div>
				</div>
				<div class="footer-col footer-col2">
					<div class="footer-title">{{ cmslabel('footer_userbox', 'title') }}</div>
					<!-- FIXME -->
					<ul class="footer-nav">
						<li><a href=""><span>Moj račun</span></a></li>
						<li><a href=""><span>Moje narudžbe</span></a></li>
						<li><a href=""><span>Uredi podatke</span></a></li>
						<li><a href=""><span>Promjeni lozinku</span></a></li>
						<li><a href=""><span>Odjava</span></a></li>
					</ul>
				</div>
				<div class="footer-col footer-col3">
					<div class="footer-stats">
						<div class="footer-title">{{ cmslabel('footer_stats', 'title') }}</div>
						<div class="footer-stats">
							<!-- FIXME -->
							<div class="footer-stats">
								<p>
									<strong>Ukupno:</strong> 2
									<span>495,10 kn</span>
								</p>

								<!-- Statistic in process -->
								<p>
									<strong>U procesu:</strong> 0
									<span>0,00 kn</span>
								</p>

								<!-- Statistic waiting payment -->
								<p>
									<strong>Čeka uplatu:</strong> 0
									<span>0,00 kn</span>
								</p>

								<!-- Statistic cancelled -->
								<p>
									<strong>Otkazano:</strong> 2
									<span>495,10 kn</span>
								</p>

								<p class="clear">
									<a class="btn btn-secondary btn-footer" href="https://b2b.cotra.hr/korisnik/my_webshoporder/">Sve narudžbe</a>
									<a class="btn btn-footer btn-footer-quickorder" href="https://b2b.cotra.hr/proizvodi/?special_view=order_form">Brza narudžba</a>
								</p>
							</div>
						</div>
					</div>
				</div>
				<div class="footer-col footer-col4">
					<div class="footer-title">{{ cmslabel('footer_contact', 'title') }}</div>
					<div class="contact-personnel-info">
						<!-- FIXME -->
						<p>
							<strong>Goran Maltarski</strong><br>
							Vaš komercijalist<br>
							<br>
							<strong>Tel:</strong> <a href="tel:+38542402084">+385 42 402 084</a><br>
							<strong>Mob:</strong> <a href="tel:+385912610012">+385 91 261 0012</a><br>
							<strong>Email:</strong>&nbsp;<a href="mailto:goran.maltarski@cotra.hr">goran.maltarski@cotra.hr</a>
						</p>
					</div>
				</div>
			</div>
			<div class="footer-row footer-row2">
				 <div class="footer-col copy"><UiCopyright>{{ cmslabel('copyright', 'title') }}</UiCopyright></div>
				 <div class="footer-col dev"><UiSignature/></div>
			</div>
		</div>
	</footer>	
</template>

<script>
export default {
	computed: {
		footerCol1Menu() {
			return this.$store.getters['cms/getMenu']('sidebar-menu')
		}
	}
}
</script>

<style lang="less" scoped>
/*------- footer -------*/
.footer{
	padding: 70px 0 50px; border-top: 1px solid @gray;
	a[href^=tel]{text-decoration: none;}
}
.footer-row{display: flex;}
.footer-col{width: 378px;}
.footer-col2{padding: 0 0 0; width: 330px;}
.footer-col3{
	font-size: 14px; line-height: 20px; width: 648px;
	p{padding: 0 0 7px 0;}
	span{float: right;}
	strong{font-weight: normal;}
}
.footer-col4{ flex-shrink: 0; width: 314px;
	a{text-decoration: underline;}
	a, a[href^=tel]{color: @textColor;}
}
.contact-personnel-info{display: flex; align-items: flex-start;
	img{margin-top: 4px; margin-right: 30px;}
	p{font-size: 14px; line-height: 21px;}
	strong{
		&:first-child{font-size: 20px; line-height: 24px;}
	}
}
.footer-title{font-size: 20px; line-height: 24px; font-weight: bold; padding-bottom: 15px;}
.footer-nav{
	list-style: none;
	li{display: block;}
	a{text-decoration: none; font-size: 14px; line-height: 20px; color: @textColor; display: inline-block; vertical-align: middle;}
	a.active, a:hover{color: @red}
}
.btn-footer{width: 160px; padding: 0; text-align: center; height: 44px; line-height: 44px; float: left; margin-top: 18px;}
.btn-footer-quickorder{float: right;}
.footer-stats{width: 340px; text-align: left; display: inline-block; vertical-align: top; margin-top: 4px;}
.footer-col1{
	img{margin-top: 30px; display: inline-block;}

}
.footer-row2{
	font-size: 12px; padding-top: 25px;
	.footer-col{flex-grow: 1;}
}
.footer-person{
	display: inline-block; vertical-align: top; width: 315px; 
	img{display: block; margin: 0 auto; border-radius: @borderRadius;}
}
.person-image{float: left; width: 120px;}
.person-content{float: right; width: 165px; font-size: 14px; line-height: 20px;}
.person-name{
	font-size: 20px; line-height: 24px; padding: 0 0 14px 0; font-weight: 500;
	strong{font-weight: 500;}
	span{display: block; font-size: 14px; line-height: 16px; font-weight: normal; padding-top: 5px;}
}
.dev{
	text-align: left; flex-grow: 0 !important; width: 324px;
	a{
		text-decoration: none; color: @textColor; .transition(opacity);
		&:hover{opacity: .6;}
	}
}
.footer-logo{background: url(~assets/images/logo.png) top left; background-size: contain; display: block; width: 89px; height: 34px; margin-top: 25px;}
/*------- /footer -------*/

@media screen and (max-width: @t) {
/*------- 1300 footer -------*/
	.footer{padding: 30px 0;}
	.footer-col{width: auto;}
	.footer-col1{width: 160px; flex-shrink: 0; flex-grow: 1;}
	.footer-col2{width: 180px; flex-shrink: 0; flex-grow: 1;}
	.footer-col3{width: auto; flex-grow: 1;}
	.footer-col4{width: auto; padding-left: 20px; flex-grow: 1;}
	.footer-person{width: auto;}
	.person-image{float: none; padding-bottom: 12px;}
	.person-content{float: none;}
	.contact-personnel-info{flex-flow: column;
		img{margin-right: 0; margin-top: 0; max-width: 110px; height: auto;}
		p{padding-bottom: 5px; line-height: 20px;}
	}
	.footer-logo{margin-top: 40px;}
	.dev{width: 18.2%; flex-shrink: 0;}
	/*------- /1300 footer -------*/
}

@media screen and (max-width: @tp) {
	/*------- 990 footer -------*/
	.footer{
		padding: 20px 0;
		.wrapper{padding: 0 20px;}
	}
	.footer-title{font-size: 18px; line-height: 21px;}
	.footer-nav{
		a{font-size: 13px;}
	}
	.person-image{display: none;}
	.footer-col{width: 130px;}
	.footer-col1{ 
		padding-bottom: 38px; position: relative; flex-grow: 0;
	}
	.footer-logo{bottom: -40px; position: absolute;}
	.footer-col2{width: 148px; padding-top: 37px; flex-grow: 0;
		.footer-title{display: none;}
	}
	.footer-col3{
		width: 248px; font-size: 13px; line-height: 20px;
		p{padding: 0 0 5px;}
	}
	.footer-stats{width: 248px;}
	.footer-col4{padding-left: 5px;}
	.btn-footer{width: 115px; font-size: 14px;}
	
	.contact-personnel-info{
		img{display: none;}
		strong{
			&:first-child{font-size: 18px; line-height: 22px}
		}
		p{font-size: 13px; line-height: 20px;}
	}
	.footer-row2{
		padding-left: 278px; padding-top: 10px; font-size: 11px;
		.footer-col.copy{width: 295px;}
		.footer-col{line-height: 18px;}
		.dev{text-align: right;}
	}
	/*------- /990 footer -------*/
}

@media screen and (max-width: @m) {
	/*------- 750 footer -------*/
	.footer{
		padding: 28px 0 22px;
		.wrapper{padding: 0 15px;}
	}
	.footer-row{flex-flow: column;}
	.footer-col{width: 100%;}
	.footer-col1, .footer-col2{display: none;}
	.footer-col3{
		order: 2; font-size: 14px; padding-top: 15px;
		.footer-title{display: block; padding-bottom: 7px;}
	}
	.footer-col4{order: 1; padding: 0;}
	.contact-personnel-info{flex-flow: row-reverse; justify-content: space-between; align-items: center;
		img{display: block; max-width: 100px;}
	}
	.footer-title{display: none;}
	.footer-person{display: flex; max-width: 395px; margin: auto;}
	.person-image{
		order: 2; display: block; width: 100px; flex-grow: 0; flex-shrink: 0;
		img{display: block; width: 100%; height: auto;}
	}
	.person-content{order: 1; flex-grow: 1; flex-shrink: 1; padding-right: 15px;}
	.person-name{
		font-size: 16px; line-height: 19px;
		span{color: #74767A; font-size: 12px; line-height: 14px; padding-top: 0;}
	} 
	.person-data{word-break: break-all;}
	.footer-stats{width: 100%;}
	.btn-footer{width: 48%; margin-top: 10px;}
	.footer-row2{padding: 0; margin: 0; font-size: 12px; line-height: 20px;}
	.footer-col.copy{order: 2; text-align: center; width: 100%!important;}
	.footer-col.dev{order: 1; text-align: center; margin-top: 16px;}
	/*------- /750 footer -------*/
}
</style>