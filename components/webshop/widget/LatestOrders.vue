<template>
	<div class="orders-cnt-bg">	
		<div class="wrapper">
			
			<div class="auth-box orders-container" id="orders">
				<h2 class="auth-title auth-title-orders"><a href="/">{{ cmslabel('latest_orders', 'title') }}</a></h2>
				
				<div class="auth-table orders">
					<div class="auth-table-header">
						<div class="table-order">
							<div class="table-col col-order-num">Broj narudžbe</div>
							<div class="table-col col-order-date">Datum</div>
							<div class="table-col col-order-status">Status</div>
							<div class="table-col col-order-qty">Količina</div>
							<div class="table-col col-order-total">Cijena</div>
							<div class="table-col col-order-btns"></div>
						</div>
					</div>
					<div class="order-row clear" id="order-458">
						<!-- Order Item -->
						<div class="table-order">
							<div class="table-col col-order-num"><span class="col-title-m">Broj narudžbe: </span>458</div>
							<div class="table-col col-order-date"><span class="col-title-m">Datum: </span>12.02.2021</div>
							<div class="table-col col-order-status"><span class="col-title-m">Status: </span>Otkazano</div>
							<div class="table-col col-order-qty"><span class="col-title-m">Količina: </span>1 kom</div>
							<div class="table-col col-order-total"><span class="col-title-m">Cijena: </span>290,00 kn</div>
							
							<div class="table-col col-order-btns">
								<a class="btn-order-details" id="btn-order-458" href="javascript:toggleBox(['div#order-458', 'a#btn-order-458']);">
									<span class="btn-inactive">Prikaži detalje</span>
									<span class="btn-active">Sakrij detalje</span>
								</a>
							</div>
						</div>

						<!-- Order Item Details (subitems) -->
						<div class="order-details clear">
							<div class="w-table w-table-details">
								<div class="wp wp-details">
										<div class="wp-image">
											<figure>
												<img src="https://b2b.cotra.hr/upload/catalog/product/3046/thumb/35915_60264c4045180_80x80r.png" width="80" height="80" alt="SVJETILJKA LED ZIDNA ANTRACIT 10W IP65 JR601A DG" data-product_main_image="3046_0">
											</figure>
										</div>
										<div class="wp-cnt">
											<h2 class="wp-title" data-product_title="3046_0">SVJETILJKA LED ZIDNA ANTRACIT 10W IP65 JR601A DG</h2>
											<div class="wp-code"><span>Šifra:</span> <span data-product_code="3046_0">35915</span></div>
											<div class="wp-qty-count">
												<span class="product_qty">1  kom</span> x 232,00 kn
											</div>
											<!-- Repeat Product Order -->
											<a class="btn btn-cart btn-order-again" href="javascript:cmswebshop.shopping_cart.add('3046_0', '', 'simple', 'simple', 3)"><span>Dodaj u košaricu</span></a>
										</div>
									</div>
								</div>
							
								<div class="wp-details-total">
									<div>
										<span class="w-totals-label">Osnovica za obračun PDV-a:</span>
										<span class="w-totals-value total_extra_payment">232,00 kn</span>
									</div>
									<div>
										<span class="w-totals-label">Ukupan PDV:</span>
										<span class="w-totals-value total_extra_payment">58,00 kn</span>
									</div>
									<div>
										<span class="w-totals-label">Ukupno bez dostave:</span>
										<span class="w-totals-value total_extra_payment">290,00 kn</span>
									</div>
									<div>
										<span class="w-totals-label">Dostava:</span>
										<span class="w-totals-value total_extra_payment">0,00 kn</span>
									</div>
									<div class="ww-total cart-total">
										<span class="w-totals-label">Ukupno za plaćanje:</span>
										<span class="w-totals-value value cart_info_total">290,00 kn</span>
									</div>
								</div>
								<a class="btn btn-purple btn-repeat-order" href="https://b2b.cotra.hr/proizvodi/?special_view=order_form&amp;order_id=1410">Uredi i ponovi narudžbu</a>
							</div>
						</div>
						<div class="clear"></div>
					</div>
				</div>
			</div>
		
		</div>
	</div>
</template>

<style lang="less">
.orders-cnt-bg{
	background: #f3f3f3; padding: 60px 0 80px;
	@media (max-width: @t){padding: 50px 0 70px;}
	@media (max-width: @tp){padding: 20px 20px 40px;}
	@media (max-width: @m){background: #fff; padding: 0;}
}
.auth-table{
	background: #fff;
	@media (max-width: @m){
		.auth-table.orders{padding: 0 15px;}
	}
}
.auth-title-orders{
	text-align: center; font-size: 28px; line-height: 33px; font-weight: bold; padding: 0 0 20px;
	@media (max-width: @m){font-size: 24px; line-height: 28px; text-align: left; padding: 25px 15px 11px; border-bottom: 1px solid @borderColor;}
	a{color: @textColor;}
}
.auth-table-header{
	background: @primaryColor; color: #fff; font-size: 18px; font-weight: 500; line-height: 36px;
	@media (max-width: @t){font-size: 16px;}
	@media (max-width: @m){display: none;}
	.col-total{font-weight: 500;}
}
.order-row { 
	position: relative; font-size: 16px; border-top: 1px solid @borderColor;
	@media (max-width: @t){font-size: 14px;}
	@media (max-width: @m){border-bottom: 1px solid @borderColor; padding: 15px 0; border-top: 0;}
	&.active .order-details { display: block; min-height: 315px;}
}
.table-col{padding: 7px 0;}
.table-order{ 
	display: table; width: 100%; 
	@media (max-width: @m){
		display: block; position: relative;
		.table-col{display: block; width: 100%!important; padding: 0; text-align: left; font-size: 14px; line-height: 22px;}
		.col-order-btns{padding-top: 4px; position: absolute; right: 0; top: 0; width: auto!important;}		
	}
	.table-col {vertical-align: middle;}
}
.col-order-num{
	padding-left: 30px;
	@media (max-width: @t){padding-left: 20px; width: 140px;}
	@media (max-width: @tp){width: 145px;}
}
.col-order-date{
	width: 255px;
	@media (max-width: @ls){width: 180px;}
	@media (max-width: @t){width: 160px;}
	@media (max-width: @tp){width: 100px;}
}
.col-order-status{
	width: 450px;
	@media (max-width: @l){width: 300px;}
	@media (max-width: @t){width: 170px;}
	@media (max-width: @tp){width: 150px;}
}
.col-order-qty{
	width: 270px;
	@media (max-width: @ls){width: 190px;}
	@media (max-width: @t){width: 130px;}
	@media (max-width: @tp){width: 88px;}
}
.col-order-total{
	width: 240px; font-weight: bold;
	@media (max-width: @t){width: 170px;}
	@media (max-width: @tp){width: 100px;}
	@media (max-width: @m){
		span{font-weight: normal;}
	}
}
.col-order-btns{
	text-align: right; width: 165px; padding-right: 10px;
	@media (max-width: @t){width: 122px;}
}
@media (max-width: @m){
	.col-title-m{display: inline;}
}
.btn-order-details{
	color: #fff; background: @secondaryColor; height: 36px; line-height: 37px; width: 100%; display: inline-block; vertical-align: top; text-decoration: none; position: relative; cursor: pointer; border-radius: 2px; font-size: 14px; font-weight: 500; padding-right: 45px; text-align: right; .transition(all);
	@media (max-width: @t){font-size: 12px; padding-right: 35px;}
	@media (max-width: @tp){font-size: 11px;}
	@media (max-width: @m){font-size: 12px; width: auto; padding: 0 30px 0 14px;}
	&:hover{text-decoration: none; color: #fff; background: @secondaryColor/1.2;}
	&:after, &:before{.pseudo(10px,2px); background: #fff; top: 17px; right: 20px;}
	@media (max-width: @m){
		&:after{right: 15px;}
	}
	&:before{
		width: 2px; height: 10px; top: 13px; right: 24px;
		@media (max-width: @m){right: 19px;}
	}
	&.active{
		&:before{display: none;}
		.btn-active { display: inline-block; }
		.btn-inactive { display: none; }
	}
	.btn-active{display: none;}
}
.order-details{
	padding: 0 30px 30px; position: relative; display: none;
	@media (max-width: @m){padding: 15px 0;}
	.wp{
		&>div{
			border: 0; padding-top: 15px; padding-bottom: 15px;
			@media (max-width: @m){padding-top: 0;}
		}
	}
	.wp-qty-count{
		padding-top: 1px; font-weight: 500; font-size: 14px; line-height: 16px;
		@media (max-width: @m){font-size: 12px;}
	}
	.wp-title{
		padding: 0 0 3px;
		@media (max-width: @t){max-width: 260px;}
	}
	@media (max-width: @tp){
		.wp-image{
			width: 95px;
			figure{width: 80px; height: 88px;}
		}		
	}
}
.btn-order-again{
	height: 40px; line-height: 42px; margin: 15px 0 0; font-size: 14px; padding: 0 18px; font-weight: 500; width: 170px; ; display: inline-block; 
	span{padding-left: 25px;
		&:before{top: -4px; left: -3px; font:18px/22px @fonti;}
	}
}
.wp-details-total{
	background: @primaryColor; width: 390px; padding: 30px 35px; float: right; border-radius: @borderRadius; position: absolute; top: 16px; right: 285px; color: #fff; font-size: 16px; line-height: 28px; 
	@media (max-width: @t){width: 340px; font-size: 14px; line-height: 24px; right: 21%; top: 8px;margin: 0; padding: 20px; font-size: 13px;}
	@media (max-width: @tp){right: 10px;}
	@media (max-width: @m){
		position: relative; top: auto; left: auto; right: auto; width: 100%; margin-top: 25px;
		&:before{display: none;}
	}
	&:after{
		.pseudo(0,0); border-left: 8px solid transparent; border-right: 8px solid transparent; border-bottom: 8px solid @primaryColor; top: -8px; right: 86px;
		@media (max-width: @tp){right: 176px;}
		@media (max-width: @m){display: none;}
	}
}
.btn-repeat-order{
	width: 100%; margin-top: 20px; font-weight: 500; background: @green;
	&:hover{background: @green/1.2}
}
.all-orders-container{
	text-align: center; padding: 30px 0 0px;
	@media (max-width: @m){padding: 15px 0 0; padding: 16px 0;}	
}

@media (max-width: @m){
	.wp-details { 
		border: 0; padding: 10px 0;
		.wp-image {left: 0;}
		&>div { margin-left: 70px; }
	}
	.btn-all-orders{width: 100%; margin: 0; width: 120px; height: 36px; line-height: 36px;}
	.wrapper-orders{padding: 0 15px 25px;}
	.w-table-details{border-top: 0;}
}
</style>