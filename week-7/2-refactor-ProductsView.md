# Today, I refactored the ProductsView component which contains filtering, validation and view switching between ProductsList and ProductDetails components.

## Actually, ProductsView contains main responsibilities but we know that a component should have a single responsibility.

## I seperated the filtering and validation logic as utility functions and imported them to use in it.

## Next, the Category filter doesn't had a specific components which represents its logic and UI. So, I seperated it as `FilterByCategory` component.

## Here is the PROOF OF BUILD:
<a href="https://github.com/HaRsHa91544/product-management-app/commit/743bc4fa1a33a2303494916c914eee7e897dd55c">Click to open it</a>