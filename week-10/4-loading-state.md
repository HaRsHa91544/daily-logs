# Today, I added a state called `stateOfProducts` to handle the products loading -> pending, success and failure states in the product management app.

## I created the state in the ProductsProvider where the main state lives and it is accessed in the ProductsList component through context.

## I tested different test cases like turning off the WIFI when products are loading, requesting to an incorrect API, removing the dB connection in the backend.

## I found that the UI is not synchronized with the loading state at failures because the useMemo hook has the dependencies as products state only. So whenever the `stateOfProducts` is updating a new Context value reference is unable to create.

## So, I fixed the issue by adding the stateOfProducts into the dependency array.

## Here is the PROOF OF BUILD:
<a href="https://github.com/HaRsHa91544/product-management-app/commit/2690693ea093b7d8bc51b825310c9fa0f844f2b2">Click to open the commit</a>