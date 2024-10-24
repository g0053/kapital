# kapital
Kapital Bank WP txpg-woocommerce-plugin


# TXPG plugin for Woocommerce
Plugin for payment via TXPG on HPP page

Tested on versions
* PHP: >=7.2
* Wordpress: 5.8.1
* Woocommerce: 6.6.1

## Functionality
* Purchase with the client entering payment data on the bank page
* When purchasing, sending purchase items to TXPG for OFD
* Tokenization of cards when purchasing
* Partial or full reversal of a purchase
* Return of a purchase

## Installation
* Copy the contents of the archive `txpg-woocommerce-plugin.zip` to the site in the folder `wp-content/plugins/txpg-gateway`
* Activate the plugin and enable the plugin in the list of plugins
* In the Woocommerce settings for the payment gateway, set values ​​for `Url`, `Order type`, `Login type`, `Login` and `Password`. Do the same for the test parameters.

**Example**
* Url: `https://payment.bank.ru:8001`
* Order type: `Order1`
* Login type: `TerminalSys`
* Login: `merchant1`
* Password: `SuperPassword!@12`

## Return/reverse purchase
* Go to the order page in the store's website admin panel
* Click on the `Return` button
* Enter the amount
* Click on the `... make a return ...` button
