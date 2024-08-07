## PSEUDOCODE

### JSON -
let data = [
    {
        "id": ,
        "name": "Product 1",
        "img": "image1.jpg",
        "desc": "description",
        "price": 100,
        "category": "categories"
      }
]

### functions: 
1. `generateShop()`:
    - Filter `shopItemsData` based on selectedCategory (if not "All")
    - Iterate through filtered products
    - For each product:
    - Check if the product exists in the cart (basket)
    - Generate HTML for each product, including product details, quantity controls, and an "Add to Cart" button
    - Update shop element with the generated HTML content displaying all products
2. `addToCart(productId)`:
    - Find product by id
    - Create a cart item with quantity 1
    - Add or update cart item in basket
    - Update localStorage
    - Update cart display
3. `removeItem(productId)`:
    - Find product in basket by id
    - Remove product from basket
    - Update localStorage
    - Update cart display
4. `updateItemQuantity(productId, quantity)`:
    - Find product in basket by id
    - Update quantity
    - Update localStorage
    - Update cart display
5. `calculateTotalPrice()`:
    - Calculate total price based on cart items and product prices
    - Return total price
6. `calculateAveragePrice()`:
    - Calculate average price of products in   shopItemsData
    - Return average price
7. `clearCart()`:
    - Clear basket
    - Update localStorage
    - Update cart display
8. `selectCategory(category)`:
    - Updates selectedCategory with the provided category
    - Calls generateShop() to update product display based on the selected category
9. `sortByPrice(order)`:
    - Validates the provided sorting order ("asc" or "desc")
    - Sorts shopItemsData based on product price (ascending or descending)
    - Calls generateShop() to update product display based on the sorted product data    

### Logic: 

1. Initialize basket from localStorage
2. Display products using generateShop()
3. Handle user interactions (add to cart, remove, update quantity, view total, checkout)
4. Update cart display and total price accordingly
5. Calculate and display average product price

- Implement error handling for invalid inputs or operations.