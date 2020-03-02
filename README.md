# BMB PIZZA
### By Neema Shiramba
#### 20/2/2020

## Description
This is an app for picking and ordering pizzas in different varieties, sizes and crust types.

## Behaviour Based Development
### Flip box
First add html with the class flip-box and repeat as many times as needed:
```
 <div class="col-md-3" id="col-1">
        <div class="flip-box" id="element5">
          <div class="flip-box-inner">
            <div class="flip-box-front">
            <h2><b>Hawaiian</b></h2>
            </div>
            <div class="flip-box-back">
              <h4><u>Hawaiian</u></h4>
              <p>Toppings:
                <ul>
                  <li>Ham</li>
                  <li>Pineapple</li>
                  <li>Mozzarella cheese</li>

                </ul>
            </div>
          </div>
        </div>
      </div>
```
Then to make it flip as intended use css.
```
.flip-box {
    width: 300px;
    height: 200px;
    border: 1px solid #f1f1f1;
  }
  
  .flip-box-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: transform 0.8s;
    transform-style: preserve-3d;
  }
  
  .flip-box:hover .flip-box-inner {
    transform: rotateX(180deg);
  }
  
  .flip-box-front, .flip-box-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
  }
  
  .flip-box-front {
    
    /*background-image: url("/images/p1.jpeg");*/
    background-repeat: no-repeat;
    background-size: cover;
   
  }
  
  .flip-box-back {
    background-image: url(/images/board2.jpeg);
    background-repeat: no-repeat;
    background-size: cover;
    transform: rotateX(180deg);
    
  }
```
To add images to each individual flip box, create an id for each flip box and add the following css. for this app I used the id element and assigned different numbers.
```
#element1{
    background-image: url(/images/p2.jpg);
    background-repeat: no-repeat;
    background-size: cover;
  }
```
### Order section
For this section I added the html form as shown below.
```
<div id="form">
                      <form>
                          <div class="row">
                              <div class="col-md-3">
  
                                  <label for="size" style="color:rgb(255, 0, 13)">Size</label>
                                  <select class="browser-default custom-select" id="size">
                                      <option value="">Choose option</option>
                                      <option value="1500">Large =ksh 1500</option>
                                      <option value="1000">Medium =ksh 1000</option>
                                      <option value="500">Small= ksh500</option>
                                  </select><br>
                              </div>
                              <div class="col-md-3">
  
                                  <label for="crust" style="color:rgb(255, 0, 13)">Crust</label>
                                  <select class="browser-default custom-select" id="crust">
                                      <option value="">Choose option</option>
                                      <option value="150">Crispy =ksh 150</option>
                                      <option value="100">Stuffed=ksh 100</option>
                                      <option value="70">Gluten-free =ksh 60</option>
                                  </select><br>
                              </div>
                              <div class="col-md-3">
  
                                  <label for="toppings" name="toppings" style="color:rgb(255, 0, 13)">Toppings</label>
                                  <select class="browser-default custom-select" id="toppings">
                                      <option value="60">Classic Magarita =60ksh</option>
                                      <option value="60">Classic Southern =60ksh</option>
                                      <option value="60">Classic Oven =60ksh</option>
                                      <option value="60">Classic Italian =60ksh</option>
                                      <option value="70">Hawaiian =70ksh</option>
                                      <option value="70">Chicken Tika =70ksh</option>
                                      <option value="70">Becon-chedder=70ksh</option>
                                      <option value="70">Chiken Fejita =70ksh</option>
                                      <option value="70">Herwin =70ksh</option>
                                      <option value="70">Silican =70ksh</option>
                                      <option value="70">California=70ksh</option>
                                      <option value="70">Chicken & Becon =70ksh</option>
                                      <option value="70">Chicago =70ksh</option>
                                      <option value="70">BBQ chicken =70ksh</option>
                                      <option value="70">Beef =70ksh</option>
                                      <option value="80">Nyalu =70ksh</option>
                                      <option value="80">Neapolitan =70ksh</option>
                                      <option value="80">Taco =70ksh</option>
                                      <option value="50">Samburu =70ksh</option>
                                      <option value="50">Splash =70ksh</option>
                                      <option value="50">Greek =70ksh</option>
                                      <option value="50">Garden =70ksh</option>
                                      <option value="50">Mushroom & Pepper =70ksh</option>
                                      <option value="50">Sundried=70ksh</option>
                                      <option value="50">Tortilla =70ksh</option>
                                      <option value="50">Creamed =70ksh</option>
                                  </select>
                              </div>
                              <div class="col-md-3">
  
                                  <label for="quantity" style="color: red">Quantity</label>
                                  <input class="form-control" type="text" name="pizza" id="quan" placeholder="0" max=""
                                      min="0">
                              </div><br><br><br><br><br><br>
                              <div class="zoom">
                              <button class="btn btn-success mx-auto d-block submit" type="submit" id="submit2"
                                  onclick="getTotalAmount();"><strong>Order</strong></button>
                                 </div>
                          </div>
                      </form>
  
```
I the added the following js to make it functional.
```
function getSizeValue() {
    var selectedValue = document.getElementById("size").value;
    return parseInt(selectedValue);
}
function getCrust() {
    var selectedCrust = document.getElementById("crust").value;
    return parseInt(selectedCrust);
}
function getToppings() {
    var selectedToppings = document.getElementById("toppings").value;
    return parseInt(selectedToppings);
}
function getQuantity() {
    var selectedQuantity = document.getElementById("quan").value;
    return parseInt(selectedQuantity);
}
function getTotalAmount() {
    var totalAmount = (getSizeValue() + getCrust() + getToppings()) * getQuantity();
    alert("You have Ordered" + getQuantity("")  +  " pizza."  +  ""  +  " The Total Amount is kshs "  +  (totalAmount)  +  ""  +  " Thank you for your order welcome again.");
    prompt("enter your location")
    alert("Your order will be delivered shortly, your delivery fee is 250/=")
    alert("Keep shopping with us.")
}
 
```
### Reviews
For the review section for the five star rating ,I used the span tag and added the link below.

```
<span class="fa fa-star checked"></span>
      <span class="fa fa-star checked"></span>
      <span class="fa fa-star checked"></span>
      <span class="fa fa-star .\checked"></span>
      <span class="fa fa-star checked"></span>
      <p>Now that's what i like to call "A GOOD PIZZA!", definetly coming back.</p>
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
```
I then added colour to the stars using css as follow 

```
 .checked {
    color: orange;
  }
```



### Known Bugs
If you find any issues in the code feel free to [click here](https://neema-bmb.github.io/pizza/)

### Technologies Used
I used:
HTML, Bootstrap, CSS, jQuery & Javascript.

### Contact me on: neemashiramba@gmail.com
I encourage anyone who has any contribution to make to this code to improve it do so. 
Live link:https://neema-bmb.github.io/pizza/


### License
App is licenced by [MIT.licensing](LICENCE.txt)
