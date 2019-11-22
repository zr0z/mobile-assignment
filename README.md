# Virtusize
## Mobile Assignment

Considering a store product whose data can be requested here:

```
https://staging.virtusize.jp/a/api/v3/store-products/215
```

And a product saved locally by the user that has the following structure:

```
{
    "id": 51595770,
    "sizes": [{
        "name": "XL",
        "measurements": {
            "height": 770,
            "bust": 623,
            "sleeve": 890,
            "collar": 450,
            "shoulder": 515,
            "waist": null,
            "hem": null,
            "bicep": null
        }
    }],
    "productType": 2,
    "isSgi": true,
    "created": "2019-11-22T11:27:27Z",
    "updated": "2019-11-22T11:27:27Z",
    "name": "Eddie Bauer XL",
    "cloudinaryPublicId": null,
    "deleted": false,
    "wardrobe": 72145326,
    "orderItem": null,
    "store": 678
}
```

Create a single view application that fetches the JSON data from the product endpoint and present the recommended size for the user based on the saved product.

![Sample UI](https://raw.githubusercontent.com/zr0z/mobile-assignment/master/assets/ui.png)

For the purpose of the assignment the `Try it on >` button can open our web widget in a `WebView` or a browser, using the following url:

```
https://staging.virtusize.jp/a/fit-illustrator/v1/index.html?detached=true&storeId=2&spid=215&lang=default
```

### Assets

Images are hosted on Cloudinary, they can be fetched using the following url structure:

```
https://res.cloudinary.com/virtusize/image/upload/t_product-large-retina-v1/{CLOUDINARY_PUBLIC_ID}.jpg
```

SGI (Survey generated items) icons are hosted on our CDN, they can be fetched using the following url structure:

```
http://static.api.virtusize.com/assets/product-types/{PRODUCT_TYPE_ID}.svg
```
