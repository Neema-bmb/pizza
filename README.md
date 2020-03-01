# BMB PIZZA
### By Neema Shiramba
#### 20/2/2020

## Description
This is an app about Delani studios. It expounds on details about us and the services we offer, through this app we display a portfolio of our our past work and last but not list enable our clients contact us. 

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
