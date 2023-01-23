<!-- ## Menu

| Burger | Price | Description |
| - | - | - |
| Spicy Crispy Chicken Sandwich | $3.59 | Designed and made completely from Scratch, one of our most popular items.|
| Stack OverFlow | $3.99 | An enormous beef burger inspired by the best forum ever. |
| Chicken Bytes | $2.39 | Byte sized chicken nuggets |
| Software Fries | $1.79 | Our world renowned soft and scrumptious fries. |
| Vegetarian burger| $3.79 | A quality option for all vegetarians, consisting of numerous vegetables and a patty made of Java beans. |

| Drink | Price | Description |
| - | - | - |
| Homebrew-ed Coffee | $2.59 | Fresh coffee brewed directly from Homebrew.  |
| URL Grey Tea | $1.99 | Our in-house specialty tea  |
| Fountain Drink | $1.00 | Your choice of our ice code sodas | -->

<html>
<head>
<style>

.menu {
  padding: 70px 25px;
  width: 93%;
  text-align: center;
}

.menu ul {
  margin: 0;
  padding: 0;
}

.menu ul li {
  color: white;
  font-size: 20px;
  text-transform: uppercase;
  letter-spacing: 3px;
}

.ItemPriceDescriptionPictureCart {
  margin: 0;
  padding: 10px 0;
}

.ItemPriceDescriptionPictureCart li {
  display: inline-block;
  width: 17%;
  color: white;
  text-align: center;
}

.info {
  padding: 10px 0;
  margin: 20;
}

.info li {
  list-style-type: none;
  display: inline-block;
  width: 15%;
  text-align: center;
  margin-bottom: 5px;
  font-size:12px;
  color: white;
}

/* Add media queries for smaller screens */
@media screen and (max-width:720px) {
  .ItemPriceDescriptionPictureCart li, .info li {width: 25.3%;}
}

@media screen and (max-width: 420px) {
  .ItemPriceDescriptionPictureCart li, .info li {width: 25.2%;}
  .info li .active {padding: 2px;}
}

@media screen and (max-width: 290px) {
  .ItemPriceDescriptionPictureCart li, .info li {width: 24.5%;}
}

</style>
</head>
<body>

<div class="menu">      
  <ul>
    <li>
       Food Menu<br>
    </li>
  </ul>
</div>

<ul class="ItemPriceDescriptionPictureCart">
  <li>Item</li>
  <li>Price</li>
  <li>Description</li>
  <li>Picture</li>
  <li>Add to Cart?</li>
</ul>

<ul class="info">  
  <li>Spicy Crispy Chicken Sandwich</li>
  <li>$3.59</li>
  <li>Designed and made completely from Scratch, one of our most popular items</li>
  <img src="/menu/SpicyCrispyChickenSandwich.png" alt="Spicy Crispy Chicken Sandwich" width="250px">
  <li>
    <input type="checkbox" id="Spicy-Crispy-Chicken-Sandwich" value="1">
  </li>
  <li>Stack OverFlow</li>
  <li>$3.99</li>
  <li>An enormous beef burger inspired by the best forum ever</li>
  <img src="/menu/StackOverflow.png" alt="StackOverflow" width="250px">
  <li>
    <input type="checkbox" id="Stack-OverFlow" value="1">
  </li>
  <li>Chicken Bytes</li>
  <li>$2.39</li>
  <li>Byte sized chicken nuggets</li>
  <img src="/menu/ChickenBytes.png" alt="Chicken Bytes" width="250px">
  <li>
    <input type="checkbox" id="Chicken-Bytes" value="1">
  </li>
  <li>Software Fries</li>
  <li>$1.79</li>
  <li>Our world renowned soft and scrumptious fries</li>
  <img src="/menu/SoftwareFries.png" alt="Software Fries" width="225px">
  <li>
    <input type="checkbox" id="Software-Fries" value="1">
  </li>
  <li>Vegetarian Burger</li>
  <li>$3.79</li>
  <li>A quality option for all vegetarians, consisting of numerous vegetables and a patty made of Java beans</li>
  <img src="/menu/VegetarianBurger.png" alt="Vegetarian Burger" width="150px">
  <li>
    <input type="checkbox" id="Vegetarian-Burger" value="1">
  </li>
</ul>

<div class="menu">      
  <ul>
    <li>
       Drinks Menu<br>
    </li>
  </ul>
</div>

<ul class="ItemPriceDescriptionPictureCart">
  <li>Drink</li>
  <li>Price</li>
  <li>Description</li>
  <li>Picture</li>
  <li>Add to Cart?</li>
</ul>

<ul class="info">  
  <li>Homebrew-ed Coffee</li>
  <li>$2.59</li>
  <li>Fresh coffee brewed directly from Homebrew</li>
  <img src="/menu/HomebrewedCoffee.png" alt="Homebrew-ed Coffee" width="250px">
  <li>URL Grey Tea</li>
  <li>$1.99</li>
  <li>Our in-house specialty tea</li>
  <img src="/menu/URLGreyTea.png" alt="URL Grey Tea" width="250px">
  <li>Fountain Drink</li>
  <li>$1.49</li>
  <li>Your choice of our ice code sodas</li>
  <img src="/menu/FountainDrink.png" alt="Fountain Drink" width="200px">
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <input type="button" value="Add to Cart" onclick="addToCart()">
</ul>


<script>
  function addToCart() {
    // Get all the checkboxes
    const checkboxes = document.querySelectorAll('input[type="checkbox"]');

    // Create an array to store the selected item IDs
    const selectedItems = [];

    // Loop through the checkboxes
    for (let i = 0; i < checkboxes.length; i++) {
      // If the checkbox is checked
      if (checkboxes[i].checked) {
        // Add the item ID to the array
        selectedItems.push(checkboxes[i].value);
      }
    }

    // Create a new XMLHttpRequest object
    const xhr = new XMLHttpRequest();

    // Open a POST request to the specified URL
    xhr.open('POST', '/add-to-cart');

    // Set the request header for sending data in the request body
    xhr.setRequestHeader('Content-Type', 'application/json');

    // Send the request with the selected item IDs as data
    xhr.send(JSON.stringify({ itemIds: selectedItems }));

    // Handle the response
    xhr.onload = function() {
      if (xhr.status === 200) {
        console.log('Items added to cart successfully!');
      } else {
        console.error('Error adding items to cart');
      }
    }
  }
</script>
