<h1><strong>FreeCode Camp - Shopping Cart</storng></h1>

## Learn Basic OOP by Building a Shopping Cart
### OOP, or Object Oriented Programming, is one of the major approaches to the software development process. In  OOP, developers use objects and classes to structure their code.

### In this shopping cart project, you'll learn how to define classes and use them. You'll create class instances and implement methods for data manipulation.

### This project will cover concepts like the ternary operator, the spread operator, the this keyword, and more.



## Step 1
### You will be building a shopping cart application. The HTML and CSS are already provided, but you will need to build the JavaScript to make the page interactive.

### To start, you will need to get some of your elements from the DOM. Start by using document.getElementById() to get the#cart-container, #products-container, and #dessert-card-container elements. Store them in variables named cartContainer, productsContainer, and dessertCards, respectively.

### Since these will not change, remember to use const to declare them.


## Step 2
### Now you need to get your two buttons. Continuing the pattern, get the #cart-btn and #clear-cart-btn elements. Store them in variables named cartBtn and clearCartBtn, respectively.


## Step 3
### Next is to get your totals. Get the #total-items, #subtotal, #taxes, and #total elements. Store them in variables named totalNumberOfItems, cartSubTotal, cartTaxes, and cartTotal, respectively.


## Step 4
### The last element to get is the #show-hide-cart element. Store it in a variable named showHideCartSpan.

### Then, use let to declare a variable named isCartShowing and set it to false.

## Step 5
### A shopping cart does not serve much purpose without products. Declare a products variable and set it to an empty array. Using an array will allow you to store multiple products.

## Step 6
### You now need to start adding products. Before you do that, you need to consider the structure of your product data. A product will need a unique identifier to distinguish it from other products, a price so people know how much it costs, and a name so people know what they are buying. You should also add a category to each product.

### Add an object to your products array. Give this object an id property set to the number 1, a name property set to the string "Vanilla Cupcakes (6 Pack)", a price property set to the number 12.99, and a category property set to the string "Cupcake".

## Step 7Passed
### Following that same data structure, add the products from this table (in order) to your products array. Increment the id for each product, counting up.

| name | price | category |
|------|-------|----------|
| French | Macaron | 3.99 |	Macaron |
|Pumpkin | Cupcake |	3.99 | Cupcake |
|Chocolate | Cupcake |	5.99 | Cupcake |
|Chocolate | Pretzels (4 Pack)	| 10.99 |	Pretzel |
|Strawberry | Ice | Cream | 2.99 | Ice Cream |
|Chocolate | Macarons (4 Pack)	9.99 | Macaron |
|Strawberry | Pretzel | 4.99 |	Pretzel |
|Butter Pecan | Ice Cream	| 2.99 | Ice Cream |
|Rocky Road  | Ice Cream |	2.99 | Ice Cream |
|Vanilla | Macarons (5 Pack) |	11.99 |	Macaron |
|Lemon | Cupcakes (4 Pack)	| 12.99 |	Cupcake |

## Step 8
### Now that you have your list of products, you can use JavaScript to insert them into the HTML. With this approach, if you decide to add more products, the HTML will automatically reflect that.

### Start by calling the .forEach method of your products array. Use arrow syntax to create an empty callback function.

## Step 9
### Remember that you can use destructuring to extract multiple values from an array or object in a single statement.

### For the first parameter of your callback function, destructure the name, id, price, and category properties from the object passed in.

## Step 10
### You need to display the available products in your HTML. Start by using the addition assignment operator to add an empty template literal string to the innerHTML property of the dessertCards variable.