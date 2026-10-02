# Today, I got a new arch problem in Product Management app and this is what I questioned and thought about the approach.

1. `selectedProductId` was moved from `App` into a new `Products` parent because `Products` is the common parent of `ProductList` and `ProductDetails`.
2. `searchValue` and `filterByCategory` were also moved into `Products` so they survive when `ProductList` unmounts.
3. `Products` accesses `products` through `ProductsContext` instead of receiving it through props.
4. `selectedProduct` is derived from `products` + `selectedProductId`, so we don't store redundant state.
5. If `selectedProduct` becomes `undefined` after deletion, `Products` conditionally renders `ProductList` again.

## I'm still building it!