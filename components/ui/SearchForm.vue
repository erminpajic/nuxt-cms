<template>
	<div class="sw">
		<a href="javascript:;" class="sw-toggle mobile"></a>
		<form class="sw-form" action="https://b2b.cotra.hr/proizvodi/" method="get">
					<input class="sw-input ui-autocomplete-input" name="search_q" id="search_q" type="text" value="" placeholder="Pretraživanje..." autocomplete="off"><span role="status" aria-live="polite" class="ui-helper-hidden-accessible"></span><span id="field-search_q-autocomplete_position" class="autocomplete-container"><ul class="ui-autocomplete ui-menu ui-widget ui-widget-content ui-corner-all" id="ui-id-1" tabindex="0" style="z-index: 101; display: none;"></ul></span>
			<button class="sw-btn" type="submit">Traži</button>
		</form>
	</div>	
</template>

<style lang="less">
.sw{
	position: absolute; top: 15px; left: 450px; width: 780px; 
	&:after{.icon-search; font: 18px/18px @fonti; color: #b3b3b3; position: absolute; left: 20px; top: 16px;}
}
.sw-form{font-size: 0;}
.sw-input{height: 50px; font-weight: normal; border: 1px solid @gray; width: 100%; font-size: 16px; padding: 0 120px 0 60px; display: block; .placeholder(#000,@gray/1.4);
	&::-webkit-search-cancel-button{display: none;}
}
.sw-btn{display: block; vertical-align: top; right: 0; top: 0; position: absolute; background: @secondaryColor; width: 98px; min-width: 98px; margin-right: 0; font-size: 16px; font-weight: 500; height: 50px; line-height: 51px; padding: 0; border-radius: @borderRadius; border-top-left-radius: 0; border-bottom-left-radius: 0; 
	&:hover{background: @secondaryColor/1.1;}
}
.sw-nocart-price{ width: auto !important; right: 0 !important;
	.sw-input{width: 100%;}
}

@media (max-width: @l){
	.sw{left: 340px; right: 450px; width: auto;}
	.sw-input{width: 100%;}	
}

@media (max-width: @t){
	.sw{left: 220px; right: 435px;
		&:after{left: 18px; font: 16px/16px @fonti; top: 17px;}
	}
	.sw-input{width: 100%; padding: 0 95px 0 50px; font-size: 14px;}
	.sw-btn{width: 80px; min-width: 80px; }	
}

@media (max-width: @tp){
	.sw{
		right: 134px; left: 292px; top: 20px;
		&:after{display: none;}
	}
	.sw-input{width: 100%; height: 47px; font-size: 14px; padding: 0 55px 0 20px;}
	.sw-btn{
		width: 47px; min-width: 47px; height: 47px; font-size: 0;
		&:before{position: absolute; .icon-search; font: 18px/18px @fonti; color: #fff; left: 14px; top: 15px;}
	}
	.sw-nocart-price{right: 77px !important;}	

	.autocomplete-container{top: 47px;}
}

@media (max-width: @m){
	.sw{
		top: 0; right: 78px; left: auto; z-index: 100;
		&.active{
			right: 0; left: 0;
			.sw-toggle{
				position: absolute; top: 0; left: 0; border-left: 0;
				&:before{.icon-x; font-size: 11px; line-height: 11px; color: #828790; top: 17px;}
			}
			.sw-form{display: block;}
		}
	}
	.sw-form{display: none;}
	.sw-toggle{
		display: block; width: 40px; height: 44px; border-left: 1px solid #E8E8E8;
		&:before{position: absolute; .icon-search; font: 14px/14px @fonti; color: @black; left: 13px; top: 15px;}
	}
	.sw-input{border: 0; height: 42px; width: 100%; padding: 0 80px 0 40px; font-size: 12px;}
	.sw-btn{
		width: 60px; height: 34px; line-height: 34px; position: absolute; top: 4px; right: 5px; font-size: 12px; border-radius: 2px;
		&:before{display: none;}
	}
	
	.sw-nocart-price{right: 41px !important;
		&.active{ right: 0 !important;}
	}	

	.autocomplete-container{top: 44px;}
}

/*------- autocomplete -------*/
.autocomplete-container{position: absolute; top: 50px; right: 0; left: 0; box-shadow: 0px 0px 25px rgba(0, 0, 0, .2); z-index: 100;}
.ui-autocomplete{
	background: #fff; list-style: none; width: auto !important; left: 0px !important; right: 0px !important; padding: 0; margin: 0; max-height: 520px; font-size: 14px; z-index: 550 !important; top: 0 !important;
	li{cursor: pointer; color: @textColor; border-top: 1px solid #E8E9F3; .transition(background-color);}
	li:first-child{border: none;}
	li:hover, .ui-state-focus{background: #efefef;}
	a{
		display: block; .clear; color: @textColor; text-decoration: none; line-height: 17px; padding: 10px; background: none;
		&:hover{color: @textColor;}
	}
	.search-title{display: block; font-weight: bold; padding: 0 0 3px 0;}
	.search-price{display: block; padding-top: 2px;}
	.image{overflow: hidden; background: #fff; float: left; width: 60px; height: 60px; line-height: 56px; margin: 0 15px 0 0; text-align: center; border: 1px solid #E8E9F3;}
	img{display: inline-block; vertical-align: middle;}
	li.autocomplete-showall{
		text-align: center; padding: 5px;
		a{.btn; width: 100%;}
	}
}
/*------- /autocomplete -------*/
</style>