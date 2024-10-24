# TXPG plugin for Woocommerce Kapital Bank
Plugin for payment via TXPG on HPP page

Tested on:
* OS: Debian GNU/Linux 11 (bullseye)
* PHP: 7.4.33
* Wordpress: 6.6.2
* Woocommerce: 9.3.3

## Functionality
* Purchase with the client entering payment data on the bank page
* When purchasing, sending purchase items to TXPG for OFD
* Tokenization of cards when purchasing
* Partial or full reversal of a purchase
* Return of a purchase

## Installation

* Download plugin:
```
wordpress=/var/www/wordpress
cd /tmp/
wget https://raw.githubusercontent.com/g0053/kapital/refs/heads/main/txpg-woocommerce-plugin.zip
```
* Extract:
```
unzip txpg-woocommerce-plugin.zip
```
* Copy extracted folder to the site in the folder `wp-content/plugins/txpg-gateway` and set ownerships:

```
cp -r ./txpg-gateway $wordpress/wp-content/plugins/
chown -R www-data:www-data /$wordpress/

```

* Activate the plugin and enable the plugin in the list of plugins; you can use wp_cli or WEB UI admin to activate the plugin:
```
# wp plugin status txpg-gateway            

Plugin txpg-gateway details:
    Name: Платёжный плагин TXPG
    Status: Inactive
    Version: 1.0.0
    Author: Sergey Ivanov


# wp plugin activate txpg-gateway

Plugin 'txpg-gateway' activated.
Success: Activated 1 of 1 plugins.
 

# wp plugin status txpg-gateway

Plugin txpg-gateway details:
    Name: Платёжный плагин TXPG
    Status: Active
    Version: 1.0.0
    Author: Sergey Ivanov
    Description: Оплата картамы через TXPG

```

* Using WEB UI in the Woocommerce settings for the payment gateway, set values ​​for `Url`, `Order type`, `Login type`, `Login` and `Password`. Do the same for the test parameters.

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
