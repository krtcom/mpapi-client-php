# Marketplace API client - change log

## 3.16.0
- added `fairPrice` attribute to `Article entity`

## 3.15.0
- added `external_id` attribute to orders
- `promotions` attribute is deprecated

## 3.14.0
- added support for batch `availability` endpoint

## 3.13.0
- added support for `energy_label` and `information_list` fields of media

## 3.12.3
- added support for `energy_label` and `information_list` fields of media

## 3.12.2
- fixed incorrect return type for `Order::getPaymentType` from `?int` to `?string`

## 3.12.1
- added support for `ulozenka_status_history` order field

## 3.12.0
- added support for `branches` order field + missing order fields

## 3.11.6
- added support for `first_delivery_attempt` order field

## 3.11.5
- reverted the changes from 3.11.1 - 3.11.4

## 3.11.4
- fixed 3.11.2

## 3.11.2
- fixed 3.11.1

## 3.11.1
- updated logging of request errors, they are no longer truncated after 120 characters

## 3.11.0
- added support for new `pricing` endpoints for Products and Variants

## 3.10.1
- added `responseCode` into ApplicationException to Products and Variants service

## 3.10.0
- added new field `mdp` in order

## 3.9.3
- fix type hint in `setApplicationTag` method

## 3.9.0
- added new field `partner_title` in product

## 3.8.3
- add option to include testing orders into orders list [orders documentation](https://github.com/mallgroup/mpapi-client-php/blob/master/doc/ORDERS.md#get-all-orders-include-testing-orders)

## 3.8.0
- added `serial-numbers` endpoint ([orders documentation](https://github.com/mallgroup/mpapi-client-php/blob/master/doc/ORDERS.md#order-item-serial-numbers))

## 3.7.0
- added `checks\media` endpoint

## 3.6.0
- added `checks` endpoint

## 3.5.1
- added option to set application tag

## 3.5.0
- added tracking url to order, changed tracking number endpoint

## 3.4.0
- option to turn off data collector

## 3.3.2
- added `mallboxAllowed` attribute to product and variant

## 3.3.1
- update version

## 3.3.0
- added new product activation method `MPAPI\Services\Products#activate($productId)`
- added new product property `MPAPI\Entity\Products\Product#getStage()`

please refer to [product documentation](https://github.com/mallgroup/mpapi-client-php/blob/master/doc/PRODUCTS.md) for details of usage, and purpose of this change.

## 3.2.0
- added /transports endpoint, which provides list of available transport services to choose from

## 3.1.0
- added package size definition for product, variant, deliveries and pickup point, see [product documentation](https://github.com/mallgroup/mpapi-client-php/blob/master/doc/PRODUCTS.md)

## 3.0.0
- delivery settings removed, use deliveries instead of delivery settings

## 2.16.0
- changed API URL to mallgroup.com

## 2.15.0
- delivered orders data was extended with 'delivered_at' field (list of basic orders data, order detail)

## 2.14.0
- added optional fourth arguments forcetoken into put method in Products service
- added optional third arguments forcetoken into put method in Variants service

## 2.13.0
- Product/Variant entity extended with 'purchase_price', one of the 'price' or 'purchase_price' is required

## 2.12.0
- added the option to enable (default) or disable auto data collecting

## 2.11.0
- changed variant media switch to string; now is media tied to variable parameters; put one of the variable parameters

## 2.10.0
- extended order detail and orders basic data with customer ID

## 2.9.0
- extended product and variant entity with option 'free delivery' that sets delivery price to zero for the whole purchase where it is contained
- added 'payment_type' info into order detail

## 2.8.0
- endpoint GET order extended with 'stats' method that provides order statistics

## 2.7.0
- added new endpoint parameter values to categories

## 2.6.0
- updated composer - moved monolog logger to required-dev dependencies
- updated order endpoints - enabled filtering to get either list of ids or list of basic data for each status

## 2.5.0
- extended variant media with 'switch', that marks media as variant color switch (method addMedia has been extended with optional parameter 'switch')
- changed Product/Variant entity method addMedia; second parameter 'main' is now optional and default value is false

## 2.4.0
- added endpoints to get list of orders by all kinds of order statuses

## 2.3.6
- added tracking number to order detail

## 2.3.5
- Bug fix: warnings in object iterator

## 2.3.4
- Bug fix: access to pickup point dimensions

## 2.3.3
- implemented data collector for product list; key 'ids' has been removed from response structure and the list of product ids is returned directly to the output

## 2.3.2
-  removed developer's URL from config

## 2.3.1
- in services the access type of client object has been changed to protected

## 2.3.0
- moved products entities into Products namespace
- added method to remove used filter
- added two types of variant lists ('ids' and 'basic'). To get list with basic data you can use filter 'basic'. Filter 'ids' is set as default.
- variants service GET returns three types of return type: 'array', 'Variant', 'BasicVariantIterator'

## 2.2.1
- fix basic product data get status

## 2.2.0
- added filtering to **Product list** to offer more data for each product
- if you need more product data in the list, you can use filters to switch response data structure

## 1.0
- Easy to use - put client id an start using
- setup new public URL
- Based on [guzzle/guzzle](https://github.com/guzzle/guzzle), [Seldaek/monolog](https://github.com/Seldaek/monolog)
- Using [Codeception](https://github.com/Codeception/Codeception) for testing
