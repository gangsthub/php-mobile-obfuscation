# php-mobile-obfuscation

Mobile Number Obfuscation for (yet another) *Wordpress* site.

This code will allow you to show your number as __simple text in desktop computers__ and as __a link in mobile phones, direct to phone calling function__ in mobile devices; meanwhile your number is always obfuscated.

You can see an example in the footer of: http://erikaabenia.com

Enjoy!

## Requires:

- PHP library *Mobile_Detect*
    - There's a *plugin* for *wordpress*: https://wordpress.org/plugins/wp-mobile-detect/

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
