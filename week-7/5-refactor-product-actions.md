# Today, I refactored the duplication code of Product Actions of ProductDetails and ProductCard which contains their responsible State, UI and logic as new component called ProductActions.

## It raised the props drilling at small scale because the setSelectedProduct setter function (stores the state of product when its view btn is clicked) is passed from ProductsView -> ProductsList -> ProductCard -> ProductActions.

## The intermediate components which are ProductsList and ProductsCard doesn't use them but we kept at ProductsView to remain the state persistent. 

## I will think a solution for it tomorrow.

## Here is the PROOF OF BUILD:
<a href="https://github.com/HaRsHa91544/product-management-app/commit/3d822758fc8096701751b89ee596a2f588311f6a">Click to open it</a>