# Today, I implemented the filtering products based on their category in the react product management app.

## Flow:
1. Extract and render all the categories as drop down.
2. User selects a category store it as state.
3. Filter the products based on selected category.
4. Render the filtered products.

## It works with searching also.

## Breaked at:
1. User selects a category and deletes all the products of the category.
2. In the UI the drop down shows `No category selected`.
3. But the `selectedCategory` state is still stores the deleted category.

## Solution: Whenever the `selectedCategory has a value` we will check if this category really exists in the `extracted current categories`. If it is not present then we will reset the selectedCategory state. So, every re-render verifies the selectedCategory's presence.

## Here is the PROOF OF BUILD:
<a href="https://github.com/HaRsHa91544/product-management-app/blob/main/public/day-6.png">Click to open it</a>