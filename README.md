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

### Part II : Full Scene

To complete Part II, fulfill the following requirements:

** In your CSS file, do the following:**
1. Style the elements on the page so that you have a full screen!
* Target the ```html``` and ```body``` elements. Set its ```margin``` property to 0 and ```box-sizing``` property to ```border-box```.
* Target the div with an id of ```container```. Set its ```height``` and ```width``` to 100%.
* Target the div with an id of ```player```. Set its ```height``` and ```width``` to auto and ```position``` to fixed.
* Target the ```img``` of the tombstone. Set its ```position``` to fixed and ```left``` and ```top``` properties to 300px.

### Part III : Prepare for Zombie Time!

To complete Part III, fulfill the following requirements:

** In your JS file, do the following:**
1. At the very beginning of your file, create the following function:
```javascript
window.onload = function() {

//The rest of your code goes in here

}
```

This ensures that our code gets run when the window loads.

2. Create variables to store your player and the container. *Hint: We want to get an element. How do we 'get' an element from our HTML to be used in our JavaScript?*

3. Now, let's check if any arrow keys are being pressed. First, create a keydown event by typing in the following:

```javascript
document.onkeydown = function() {

//More code in here

}
```

* But we're not done yet! We need to check which key is being pressed. Place the special word ```event``` as a parameter for this function. *Where do we place parameters (arguments) in our functions?*

* Inside of this function, create a **Switch Statement** that takes in ```event.keyCode``` and checks for our arrow key codes. Take a look at how to create Switch Statements here: https://www.w3schools.com/js/js_switch.asp. *Hint: Each case in our switch statement will have a number that corresponds with the up, down, right, and left arrow keys. This number is the key code we are looking for! What are the key codes for our arrow keys?*

* For now, check to make sure that your window is detecting the arrow keys being pressed. How can we check this?
