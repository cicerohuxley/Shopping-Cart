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

## Step 11
### In your template literal, create a div element with a class of dessert-card. In that div, create an h2 element and give it the text of the name variable.

## Step 12 
### After your h2 element, create two p elements. Give the first a class of dessert-price, and set the text to a dollar sign "$" followed by the value of the price variable. Give the second a class of product-category, and the text "Category: " followed by the value of the category variable.

## Step 13
### Finally, after your p elements, create a button element. Give it an id set to the value of the id variable, a class of btn add-to-cart-btn, and use "Add to cart" for the text.


## Step 14
### You are already familiar with an HTML class, but JavaScript also has a class. In JavaScript, a class is like a blueprint for creating objects. It allows you to define a set of properties and methods, and instantiate (or create) new objects with those properties and methods.

### The class keyword is used to declare a class. Here is an example of declaring a Computer class:

### Example Code
#### class Computer {};
#### Declare a ShoppingCart class.


## Step 15
### Classes have a special constructor method, which is called when a new instance of the class is created. The constructor method is a great place to initialize properties of the class. Here is an example of a class with a constructor method:

### Example Code
#### class Computer {
####  constructor() {
####  }
#### }
### Add an empty constructor method to the ShoppingCart class.


## Step 16
### The this keyword in JavaScript is used to refer to the current object. Depending on where this is used, what it references changes. In the case of a class, it refers to the instance of the object being constructed. You can use the this keyword to set the properties of the object being instantiated. Here is an example:

### Example Code
#### class Computer {
####     constructor() {
####      this.ram = 16;
####    }
####   }
#### In your constructor, use the this keyword to set the items property to an empty array. Also, set the total property to 0, and the taxRate property to 8.25.


## Step 17
### Your ShoppingCart class needs the ability to add items. Create an empty addItem method, which takes two parameters: id and products. Creating a method might look like this:

### Example Code
#### class Computer {
####   constructor() {
####     this.ram = 16;
####   }

####   addRam(amount) {
####     this.ram += amount;
####   }
#### }
### The first parameter, id, is the id of the product the user has added to their cart. The second parameter, products, is an array of product objects. By using a parameter instead of directly referencing your existing products array, this method will be more flexible if you wanted to add additional product lists in the future.

## Step 18
### You need to find the product that the user is adding to the cart. Remember that arrays have a .find() method. In your addItem function, declare a product variable, and assign it the value of calling the .find() method on the products array.

### For the callback to .find(), pass a function that takes a single parameter item, and returns whether the id property of item is strictly equal to the id parameter passed to addItem.


## Step 19
### Use const and destructuring to extract name and price variables from product.


## Step 20
### Now you need to push the product into the cart's items array. Remember to use the this keyword.

## Step 21
### You now need a total count of each product that the user has in the cart. Declare a totalCountPerProduct variable, and assign it an empty object.

## Step 22
### Use the .forEach() method to loop through the items array. Pass an empty callback function that takes a single parameter dessert.


## Step 23
### You’re on the right track! However, let’s take a moment to address a common issue when working with objects in JavaScript.

### When you try to access an object property that doesn’t exist, JavaScript returns undefined. If you then attempt to perform arithmetic operations on undefined, it can lead to unexpected results, such as NaN.

### To prevent this, you can use the || (logical OR) operator to provide a default value.

### Example Code
|-------------------------------------------|
####  let scores = {}; 
####  let players = ["Alice", "Bob", "Charlie"];

####  players.forEach(player => {
####    scores[player] = scores[player] || 0;
####  });
|-------------------------------------------|

### Now, let’s apply this concept to your totalCountPerProduct object in the forEach callback. Make sure that each dessert.id property is initialized properly.

### Initialize totalCountPerProduct[dessert.id] with a default value of 0 using the || operator.

## Step 24
### In the forEach callback, wrap the right-hand assignment totalCountPerProduct[dessert.id] || 0 in parentheses () to ensure proper evaluation, then increment the value by one.

## Step 25
### Now you need to get prepared to update the display with the new product the user added. Declare a currentProductCount variable, and assign it the value of the totalCountPerProduct object's property matching the id of product.

## Step 26
### You haven't written the code to generate the HTML yet, but if a product has already been added to the user's cart then there will be a matching element which you'll need.

### Use .getElementById() to get the matching element - you'll be setting the id value to product-count-for-id${product.id}, so use a template literal to query that value.

### Assign your query to a currentProductCountSpan variable.

## Step 27
### The behaviour of the addItem method needs to change if the product is already in the cart or not. Create a ternary that checks if the current product is already in the cart. Use undefined for both the truthy and falsy expressions to avoid a syntax error.

## Step 28
### For your truthy expression, removing the undefined, you need to update the textContent of the currentProductCountSpan to be the currentProductCount followed by an x. Use a template literal to do so.

## Step 29
### For your falsy expression, you'll need to add new HTML to your productsContainer. Start by removing the undefined, then use the addition assignment operator and template literal syntax to add a div with the class set to product and the id set to dessert${id} to the innerHTML property of the productsContainer.

## Step 30
### Inside your div, add two p elements. Set the text of the second p element to be the value of the price variable.















