# Woocommerce Payment Display with card Grid View CSS

## Global CSS
```
.woocommerce-checkout #order_review #payment ul.payment_methods li.wc_payment_method{
		display: inline-block;
    width: 46%;
    border-radius: 10px;
	  margin: 0 10px 10px 0px;
	  background-image: url(/wp-content/uploads/2023/01/1378126.webp); 
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    padding: 10px 0 20px 20px;
    box-shadow: 0 1px 5px 0 rgb(0 0 0 / 30%)
}
.payment_methods .payment_box{
	display: none !important;
	}
.payment_methods li>label{
	font-size: 0px;
}
.payment_methods li img{
	max-height: 60px;
	margin-top: 5px;
}
```
## Mobile Version CSS
```
.woocommerce-checkout #order_review #payment ul.payment_methods li.wc_payment_method{
	margin: 0 10px 10px 0px;
}
.payment_methods li img{
	max-height: 40px;
	max-width: 100px;
	margin-right: 2px;
  margin-left: 0px;
}
.woocommerce-checkout #order_review #payment ul.payment_methods li:nth-child(3){
	margin-top: 0px;
}
```
