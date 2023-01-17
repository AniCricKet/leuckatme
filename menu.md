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

.ItemPriceDescription {
  margin: 0;
  padding: 10px 0;
}

.ItemPriceDescription li {
  display: inline-block;
  width: 30%;
  color: white;
  text-align: center;
}

.info {
  padding: 10px 0;
  margin: 0;
}

.info li {
  list-style-type: none;
  display: inline-block;
  width: 30%;
  text-align: center;
  margin-bottom: 5px;
  font-size:12px;
  color: white;
}

/* Add media queries for smaller screens */
@media screen and (max-width:720px) {
  .ItemPriceDescription li, .info li {width: 25.3%;}
}

@media screen and (max-width: 420px) {
  .ItemPriceDescription li, .info li {width: 25.2%;}
  .info li .active {padding: 2px;}
}

@media screen and (max-width: 290px) {
  .ItemPriceDescription li, .info li {width: 24.5%;}
}

</style>
</head>
<body>

<div class="menu">      
  <ul>
    <li>
       Burger Menu<br>
    </li>
  </ul>
</div>

<ul class="ItemPriceDescription">
  <li>Burger</li>
  <li>Price</li>
  <li>Description</li>
</ul>

<ul class="info">  
  <li>Spicy Crispy Chicken Sandwich</li>
  <li>$3.59</li>
  <li>Designed and made completely from Scratch, one of our most popular items</li>
  <li></li>
  <li></li>
  <li></li>
  <li>Stack OverFlow</li>
  <li>$3.99</li>
  <li>An enormous beef burger inspired by the best forum ever</li>
  <li></li>
  <li></li>
  <li></li>
  <li>Chicken Bytes</li>
  <li>$2.39</li>
  <li>Byte sized chicken nuggets</li>
  <li></li>
  <li></li>
  <li></li>
  <li>Software Fries</li>
  <li>$1.79</li>
  <li>Our world renowned soft and scrumptious fries</li>
  <li></li>
  <li></li>
  <li></li>
  <li>Vegetarian Burger</li>
  <li>$3.79</li>
  <li>A quality option for all vegetarians, consisting of numerous vegetables and a patty made of Java beans</li>
</ul>

<div class="menu">      
  <ul>
    <li>
       Drink Menu<br>
    </li>
  </ul>
</div>

<ul class="ItemPriceDescription">
  <li>Drink</li>
  <li>Price</li>
  <li>Description</li>
</ul>

<ul class="info">  
  <li>Homebrew-ed Coffee</li>
  <li>$2.59</li>
  <li>Fresh coffee brewed directly from Homebrew</li>
  <li></li>
  <li></li>
  <li></li>
  <li>URL Grey Tea</li>
  <li>$1.99</li>
  <li>Our in-house specialty tea</li>
  <li></li>
  <li></li>
  <li></li>
  <li>Fountain Drink</li>
  <li>$1.49</li>
  <li>Your choice of our ice code sodas</li>