# Today, I made the ProductForm component in the product manangement app to mount and unmount or render conditionally when product is adding or editing.

## I created a state and used context to make it accessible to the lowest component of the React components tree.

## And I tested the feature but it got breaked, the productForm state was not cleared or synchronized with the formOpened state. When a product is editing and if the form is closed the productForm remains same. I solved this bug today.

## Here is the PROOF OF BUILD:
<a href="https://github.com/HaRsHa91544/product-management-app/blob/main/public/day-22.png">Click to open image</a>
<a href="https://github.com/HaRsHa91544/product-management-app/commits/main/?since=2026-10-12&until=2026-10-12">Click to open commits</a>