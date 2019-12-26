# magento2-images-order-items
With default Magento 2 installation, if you want to get the order details using Rest API, it will return you the complete details of the order but no product image with order items.

In order to fix this issu, I have developed this small extension that can return the product thumbnail image with order items.

##Problem
1. Call the Magento 2 REST endpoint `rest/V1/orders/orderId`
2. It will return the order details with order items
3. You can see that the product thumbnail is missing from the items

##Installation
1. Upload the folder `NA` folder to the Magento installation `app/code` Directory
2. Enable the Module using `php bin/magento module:enable NA_OrderApi`
3. Run setup upgrade command `php bin/magento set:up`
4. Run setup di compile command `php bin/magento s:d:c`
5. Clear the cache `php bin/magento c:c` and/or `php bin/magento c:f`
6. Call the API endpoint and it will return the full product thumbnail url in response.