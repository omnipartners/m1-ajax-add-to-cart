Magento Ajax Add to Cart extension
====================================================================================

Technical Details
------------------------------------------------------------------------------------

* Name: Omni_AjaxAddToCart
* Version: 0.0.0.1
* Dependencies: Mage_Checkout
* Tested On: Magento CE 1.9.2.4

Summary
------------------------------------------------------------------------------------

Unobtrusive Ajax Add to Cart extension for Magento ( RWD theme only). This extension does not override Magento template files. Instead, it is:

1. reading the normal Magento output `button.btn-cart` for correct add to cart URL's `onclick`
2. prevents default onclick handlers for add to cart buttons
3. executes ajax requests with URL's collected during the first step
4. updates the minicart content and open the minicart as visual notification

This approach enables extension to work with wide range of other extensions with as little as possible conflicts. Performance is not degraded, since ajax calls are identical to what Magento would execute by default.



Installation
------------------------------------------------------------------------------------

1. Clear the store cache under var/cache and all cookies for your store domain. Disable compilation if enabled. This step eliminates almost all potential problems. It’s necessary since Magento uses cache heavily.
2. Backup your store database and web directory.
3. Download and unzip extension contents on your computer and navigate inside the extracted folder.
4. Using your FTP client upload content of "app" & "skin" directories to "app" & "skin" directories inside your store root.

Configuration
------------------------------------------------------------------------------------

The extension provides the (Global) system configuration flag (**System->Configuration->Sales->Checkout->Shopping Cart->Enable Ajax Add to Cart**), for enabling/disabling Ajax Add To Cart functionality.
Ajax Add to Cart must be explicitly enabled in configuration, before it becomes functional on the store front.

Uninstall
------------------------------------------------------------------------------------

* You can safely remove the extension files from your store.


Testing
------------------------------------------------------------------------------------

* Open the product listing page and test "Add To Cart" and "View Details" buttons.
* Open the product details page and test "Add To Cart" button with different options selected 