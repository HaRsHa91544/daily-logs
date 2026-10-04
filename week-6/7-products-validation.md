# Today, I implemented 2 new features in product management app:
1. The validation errors for product list while searching and filtering.
2. The product form reset functionality.

## In the first feature I'm verifying wheather the products actually present in the state or not after verifying the searching and filtering states which is a bad practice.
- And I realised that the validation should begin from basic core state of an app.

## In the second feature it got broken like I observed a strange behaviour that whenever I'm clicking the reset button, a new product with default productForm state is adding.
- The reason behind it is the Button inside the form is acting as a submit button and it is calling submit handler and adding the product into the state. So, I fixed it.

## Here is the PROOF OF BUILD:
<a href="https://github.com/HaRsHa91544/product-management-app/commits/main/?since=2026-10-04&until=2026-10-04">Click to open it</a>