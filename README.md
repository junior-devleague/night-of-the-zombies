# Night of the Zombies

October is here... and so are the zombies!

![Zombie](https://github.com/junior-devleague/night-of-the-zombies/blob/master/assets/zombie.gif)

## Objective

Create a turn based game using **Keyboard Events** to detect arrow key presses and **JavaScript Functions** to check where the player is currently at. Periodically spawn zombies as **Objects** and use **Arrays** to store these objects.

## Prerequisites

To complete this project, students should have the following:
* Basic understanding of HTML structures and attributes.
* Basic understanding of JavaScript Objects, Arrays, Events and DOM.

## Your Challenge

### Part I : Set Up the Game Scene

To complete Part I, fulfill the following requirements:
1. Set up your project file structure through the command line.
2. Create the following:
* HTML file
* CSS file
* JS file
3. Link all of your files correctly.

**In your HTML file, create the following:**

**In the HTML ```body```, create:**
*  A ```div``` with an ```id``` of "container".

**In the ```div``` with an ```id``` of "container", create:**
* A ```div``` with an ```id``` of "player" that contains an ```img``` of the batman file stored in the ```assets``` directory. Set the ```width``` and ```height``` of this image to "60px".
* An ```img``` of the tombstone file stored in the ```assets``` directory. Set the ```width``` and ```height``` of this image to "50px". Set the ```id``` of this image to ```tombstone```.

------------------------------------------------

### Part II : Full Scene

To complete Part II, fulfill the following requirements:

**In your CSS file, do the following:**
1. Style the elements on the page so that you have a full screen!
* Target the ```html``` and ```body``` elements. Set its ```margin``` property to 0 and ```box-sizing``` property to ```border-box```.
* Target the div with an id of ```container```. Set its ```height``` and ```width``` to 100%.
* Target the div with an id of ```player```. Set its ```height``` and ```width``` to auto and ```position``` to fixed.
* Target the ```img``` of the tombstone. Set its ```position``` to fixed and ```left``` and ```top``` properties to 300px.

------------------------------------------------

### Part III : Prepare for Zombie Time!

To complete Part III, fulfill the following requirements:

**In your JS file, do the following:**
1. At the very beginning of your file, create the following function:
```javascript
window.onload = function() {

//The rest of your code goes in here

}
```

This ensures that our code gets run when the window loads.

2. Create variables to store your player and the container. *Hint: We want to get an element. How do we 'get' an element from our HTML to be used in our JavaScript?*

3. Create a variable called ```playerLeft```. Set that equal to 0. This will help us keep track of how far our player is from the left of the screen.

4. Create a variable called ```playerTop```. Set this equal to 0. This will help us keep track of how far our player is from the top of the screen.

5. Now, let's check if any arrow keys are being pressed. First, create a keydown event by typing in the following:

```javascript
document.onkeydown = function() {

//More code in here

}
```

* But we're not done yet! We need to check which key is being pressed. Place the special word ```event``` as a parameter for this function. *Where do we place parameters (arguments) in our functions?*

* Inside of this function, create a **Switch Statement** that takes in ```event.keyCode``` and checks for our arrow key codes. Take a look at how to create Switch Statements here: https://www.w3schools.com/js/js_switch.asp. *Hint: Each case in our switch statement will have a number that corresponds with the up, down, right, and left arrow keys. This number is the key code we are looking for! What are the key codes for our arrow keys?*

* Check to make sure that your window is detecting the arrow keys being pressed. How can we check this?

6. When we press the up arrow key, we want our player to move up. When we press the down arrow key, we want our player to move down. Think about what this means in terms of our top and left values. If we press the up arrow, we want the distance from the top of our window to decrease. If we press the down arrow, we want the player to get farther away from the top of our window. In each of the cases for your Switch Statement, decrease or increase your top and left values and change the player's position as follows:

Ex.
```javascript
playerLeft = playerLeft - 10;
player.style.left = playerLeft + 'px';
```

------------------------------------------------

### Part IV : Create a Zombie Constructor

To complete Part IV, fulfill the following requirements:

**In your JS file, do the following:**
1. Create an **Object Constructor** called ```zombie``` that will serve as a template for us to create more zombies!
2. In this Object Constructor function, define the following parameters:
* element
* speed
* height
* width
* left
* top

*Hint: Check out this link to brush up on Objects https://www.w3schools.com/js/js_object_definition.asp. Look at the example for an Object Constructor function and see how new objects can be made by using this constructor. An object constructor defines the ingredients we need to make a specific object.*

3. Create 4 **Object Methods** in your object constructor. Name the methods: ```highleft```, ```lowleft```, ```hightop```, ```lowtop```. In our game, we want the zombie to follow our player at every step the player makes. So, we need to check and compare the zombie's position to the player's position. If the zombie is more left than the player (highleft), what will we need to do to our zombie's position to make it closer to the player?

In each method, you will be using either ```left``` or ```top```, ```speed```, and ```element```.

For example, if our zombie is more left than the player (highleft), we need to decrease this left value so that the zombie is closer to our player as follows:
```javascript
this.highleft = function() {
  this.left = this.left - this.speed;
  element.style.left = this.left + 'px';
}
```

Remember, these methods are functions in our Object Constructor. So, any object that we create using this constructor will have access to these methods.

------------------------------------------------

### Part V : Moar Zombiezzzz!

1. Define a global variable called ```z1```. This variable will help us spawn zombies later on.
2. Define an empty array called ```arr```.
2. Create a function called ```spawn```.
3. In this function, do the following:
* Create a variable ```zom``` that will create an ```img``` element. *Hint: https://www.w3schools.com/jsref/met_document_createelement.asp*
* Create a variable called ```zombieLeft``` and set that equal to 300.
* Create a variable called ```zombieTop``` and set that equal to 300.
* Create a variable called ```randomSpeed``` and set that equal to ```Math.random()*5```.
* Set ```zom.src``` equal to the path of the zombie picture.
* Set ```zom.style.height``` equal to 50px.
* Set ```zom.style.width``` equal to 30px.
* Set ```zom.style.position``` equal to ```absolute``` so we can control the zombie's position using its left and top properties.
* Set ```zom.style.left``` equal to the left value plus 'px'. (Ex. ```zom.style.left = left + 'px'```)
* Set ```zom.style.top``` equal to the top value plus 'px'.
4. Create a new object using the ```zombie``` Object Constructor and set that equal to the variable ```z1```. This object will take in the following parameters:
* zom
* randomSpeed
* zom.style.height
* zom.style.width
* zombieLeft
* zombieTop
5. Push this object into the empty array ```arr```. *Hint: https://www.w3schools.com/js/js_array_methods.asp How do we push objects into an array? Do we use quotation marks?*
6. Append the child ```zom``` onto the container. Since we created this in our JavaScript file and it was not originally on our page, we need to "append" this new element onto an existing element in our window. *Link for more information: https://www.w3schools.com/jsref/met_document_createelement.asp*
7. Call your function! *What's the difference between calling and defining a function? https://www.w3schools.com/js/js_functions.asp*

------------------------------------------------

### Part VI : Zombie Overrun
1. Create a variable called ```interval``` that will set an interval for our spawn function every 5000 milliseconds.  *https://www.w3schools.com/jsref/met_win_setinterval.asp*
2. Create a function called ```check``` that will take in ```array``` as a parameter.
3. In this function, create a for loop that will go through the length of the array. *https://www.w3schools.com/js/js_loop_for.asp*
4. Remember, the array we will be putting in this function is the array of zombies that we've created previously. The zombies were objects and each object had its own properties and methods! In this check function, we are going to check where our zombie's position is in comparison to our player. We did this before!

If the zombie's distance from the top of the window is less than the player's distance from the top of the window, which method do we want to call?

Hint:
```JavaScript
if (array[i].top < playerTop) {
  console.log('lowtop');
  array[i].lowtop();
}
```

5. When will the player be eaten? Create an if statement that will account for this special case. 
