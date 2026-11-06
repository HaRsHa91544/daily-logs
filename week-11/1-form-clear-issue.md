# Today, I fixed a small issue in the product management app which is the input data in the form is cleared even when there is a Failure in the API service of Add or Update product service.

## The productSubmitHandler in ProductForm component is calling clearProductForm() right after calling saveProduct() action without any clear acknowledgement from the action.

## Now, I solved it using Promise.reject() from async saveProduct() and calling the clearProductForm() from productSubmitHandler only the promise is resolved.

## Here is the PROOF OF BUILD:
<a href="https://github.com/HaRsHa91544/product-management-app/commit/52d9783e39ecbc0942ef689a0d32f032a2a911a0">Click to open the commit</a>