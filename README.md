# Woocommerce Payment Display with card Grid View CSS

## Main Code
```
// Woocommerce Payment Display with card Grid View CSS
function custom_checkout_styles() {
    // Custom CSS for radio buttons and labels
    echo "
    <style>
        /* Remove default radio buttons */
        .woocommerce-checkout #payment ul.payment_methods input[type='radio'] {
            display: none;
        }

        /* Style for the payment method label */
        .woocommerce-checkout #payment ul.payment_methods label {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 10px 35px;
            border-radius: 5px;
            cursor: pointer;
        }

        /* Add border highlight to the selected payment method label */
        .woocommerce-checkout #payment ul.payment_methods input[type='radio']:checked + label {
            border: 3px dashed rgb(72, 118, 202);
            padding: 10px 35px;
            border-radius: 5px;
        }

        /* Grid Layout for Payment Method CSS Start */
        .woocommerce-checkout #order_review #payment ul.payment_methods li.wc_payment_method {
            display: inline-block;
            width: 48.5%;
            border-radius: var(--wd-brd-radius);
            margin: 0 2px;
            background-image: url(/wp-content/uploads/2023/03/element-background-image.svg);
            background-position: center center;
            background-repeat: no-repeat;
            background-size: cover;
            padding: 0;
            box-shadow: 0 1px 5px rgb(0 0 0 / 30%);
            background-color: white;
            text-align-last: center;
        }

        .payment_methods .payment_box {
            display: none !important;
        }

        .payment_methods li>label {
            font-size: 0;
        }

        .payment_methods li img {
            max-height: 100%;
        }
        
        .payment_methods {
            text-align-last: center;
        }
    </style>
    ";
}
add_action('wp_head', 'custom_checkout_styles');

function custom_checkout_scripts() {
    // Enqueue jQuery (if not already enqueued by your theme or plugins)
    wp_enqueue_script('jquery');

    // Custom JavaScript
    echo "
    <script>
        jQuery(function($) {
            $('#payment ul.payment_methods').on('click', 'label', function() {
                $(this).siblings('label').removeClass('selected');
                $(this).addClass('selected');
            });
        });
    </script>
    ";
}
add_action('wp_footer', 'custom_checkout_scripts');
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
