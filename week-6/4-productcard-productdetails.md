# Today, I got introduced a architectural problem in product management app and I fixed it today.

## Problem: `ProductCard` has 2 responsibilities: List item in ProductList, Displays all Details of product but a component should have only single responsibility.

## Solution: Seperating the details responsibilty from ProductCard to `ProductDetails` but ProductCard has edit and delete logic and we need to duplicate it again in the `ProductDetails`. 

### To solve I seperated the logic using custom hooks because the logic needs context of products and productForm. So, we can `useContext` only in components or custom hooks.

## Here is PROOF OF BUILD:
<a href="http://github.com/HaRsHa91544/product-management-app/commit/a4a94c528e03366ade6954e0b73e8564a4780b5d">Click to open it</a>