# Today, I refatored the ProductsList component which has multiple responsibilities like searching, filtering and validation logics inside it but it has to be have single responsibility which is to display the products.

## I shifted all the logic into ProductsView Component which is a parent component of it and maintains the state and logic related to the products.

## Here is the PROOF OF BUILD:
<a href="https://github.com/HaRsHa91544/product-management-app/commit/9a70b63e71a32db3744638e546c38f571c49ce5c">Click to open it</a>