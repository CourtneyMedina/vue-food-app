# vue-food-app

# This project is going to be a food app where users can have a starting value amount and add a quantity of various foods to their "cart" and it'll deduct it from their wallet amount
1) Create a new project called "vue-food-app" 
1.1) This app will use bootstrap css framework, so add it to our index.html
2) This app will have a few components: 
  2.1) Navbar: a navbar component with 2 buttons "Home", "Menu" and a small div on the right hand side (look up float: right on bootstrap) with "Wallet: $60"
  2.2) The wallet component's value will be whatever set as the starting value in the initially set up in the app 
  2.3) Card: the cards will display the data "product" as the product's name, the Manufacturer, the rating as a number and the price in USD format "$2.00" "$10.00" 
    1) Each card will have a unique quantity value with a plus and minus - / + and that will increment the quantity for that specific item, and as people increase the quantity of the item it will deduct from the wallet value. 
    2) If they try to add a quantity when they have insufficient funds, they should be prevented from adding it, and it should show some error message saying "You have insufficient funds" 
    3) If a user removes an item or deducts the quantity, they should get that value added back to their wallet amount 
3) we should keep an array of objects named "Cart" that will get updated with the name of the product and the quantity being ordered. Example: 
Cart : [
  {"5 Hour Energy Pomegranate": 5}, {"Monster Energy Drink": 10}, { ... }, { ... }
]

The list of objects, you can either just put in your assets folder and learn by googling, how to include a file like `let foods = require('assets/foods.json')` OR you can copy paste the entire array of objects into your App.vue


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
