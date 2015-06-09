# Add a product to the cart automatically

You can set up your cart to automatically include a product as a gift. The product is added automatically when any other item is added to an empty cart.

To add a product to your cart automatically:

* [Grab the handle of your add-on product](#grab-product-handle)
* [Create a new snippet](#create-snippet)
* [Include the new snippet in your cart template](#include-snippet)

This customization is not possible if your cart uses Ajax. If you use any of the following themes: Solo, Pop, React, Classic, Supply or Brooklyn, by Shopify, you must disable Ajax on your [Customize theme page](http://www.shopify.com/admin/themes/current/editor). In the **Cart page** section, set "Cart type" to "Page".

<h2 id="grab-product-handle">Grab the handle of your add-on product</h2>

On the product page, under **Search engine listing preview**, click the *Edit website SEO* link.

The product handle is shown under 'URL and handle':

![Alt text](https://monosnap.com/file/k2xFhnnXbz0DFJKaD3WrRJqHDv1qFK.png)

In the above example, the handle is `surprise-gift-35-value`. You will need that handle later.

<h2 id="create-snippet">Creating a new code snippet</h2>

1. Go to the [Edit HTML/CSS page](https://docs.shopify.com/manual/configuration/store-customization/#template-editor).

2. Click the **Snippets** folder, then click **Add a new snippet**.

3. Give your snippet the name `cart-add-on` and click **Create snippet**. Your new code snippet file will automatically open in the online code editor.

4. Copy the code from this project's cart-add-on.liquid file into your snippet.

5. Look for the following text:

   `put-your-product-handle-here`

   Replace that text with the product handle you grabbed before.

6. Click **Save** to save your new code snippet.

<h2 id="include-snippet">Including the new snippet in your cart template</h2>

Now you must edit your cart.liquid template to include your new code snippet.

1. Under the **Templates** folder, locate and click on _cart.liquid_ to open it in the online code editor.

2. Copy the below code at the top of your cart.liquid snippet:

   `{% include 'cart-add-on' %}`
   
3. Click **save**.
