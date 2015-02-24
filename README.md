# php-mobile-obfuscation

Mobile Number Obfuscation for (Yet Another) Wordpress site

## Requires:

- PHP library Mobile_Detect
    - There's a plugin for wordpress: https://wordpress.org/plugins/wp-mobile-detect/

## Usage

Remember to substitute asteriscs (and "+11") by your desired number (and country code).

```php
<?php
	$mobile_number_prefix = "***";
	$mobile_number = "******";
	if ( wp_is_mobile() ) {
		echo ' Tel. <a href="tel:+11' , $mobile_number_prefix , $mobile_number , '">+11', $mobile_number_prefix , $mobile_number , '</a>.';
	}else{
		echo 'Tel. ' , $mobile_number_prefix , $mobile_number , '.';
		}
?>
```
