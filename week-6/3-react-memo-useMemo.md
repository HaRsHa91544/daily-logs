# Today, I understand and implemented the memo API and useMemo Hooks in the product management app.

## Why memo API used?
- The `ProductsList` and `ProductForm` components are rerendered when there is change in any state in `App` which is not depended by them.
- Here, `memo` helps to render the `ProductsList` and `ProductForm` when there is change in their props avoiding unnecessary renders.

## Why useMemo Hook is used?
- There is a problem that `ProductsContext` and `ProductFormContext` in the app has an object reference as a value.
- The new reference is created in every render regardless of change in `products` and `productForm` state in app which causes change in context and triggers a render in `ProductsList` and `ProductForm`.
- To solve this problem I used useMemo which will create a new reference for context value whenever the `products` and `productForm` state's reference is modified.

## Here is the PROOF OF BUILD:
```javascript
const productsContextValue = useMemo(() => {
        return { products, setProducts };
    }, [products]);

const productFormContextValue = useMemo(() => {
    return { productForm, setProductForm };
}, [productForm]);
```