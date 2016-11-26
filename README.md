# Michael's Money Machine

[![N|Solid](https://github.com/pscott-au/money-machine/blob/master/assets/img/money_anim.gif?raw=true)](https://github.com/pscott-au/money-machine)

Michael's Money Machine is a learning excercise for a beginner Javascript programmer with the aim of creating a simple game similar to [Cookie Clicker](http://orteil.dashnet.org/cookieclicker/).

Here I am aiming to include all the final files and a description of the steps I took to learn what what needed to make this game.

You can see a live version of the latest version at [mms.wwww.com.au](http://mms.wwww.com.au)

## Background Learning
 * http://www.w3schools.com/html/
 * http://www.w3schools.com/js/
 * http://www.w3schools.com/css/
 * http://www.w3schools.com/jquery/
 * http://www.w3schools.com/bootstrap/
 
Working through the W3Schools free online courses will give you the background you need to understand all the material.

# First Stage - Creating the Core of the Game

## Goal 1 - The Game Loop

The game needs to continue processing and so we create a Javascript main loop using a timer that calls a function every second.
````js
function when_timer_ticks()
{
    // DO OUR STUFF THEN RESET THE TIMER TO CALL AGAIN IN ANOTHER 1000ms (1 second)
    timer = window.setTimeout( function(){ when_timer_ticks(); }, 1000 );
}

 $( document ).ready(function() // THIS IS THE MAIN CODE STARTING BLOCK
 {
   var timer = window.setTimeout( function(){ when_timer_ticks(); }, 1000 );
 }
````
 
 This code is contained in the main HTML file.

## Goal 2 - Update the screen whenever the timer ticks (each second)

Within the when_timer_ticks() function we make a call to redraw_screen();


## Goal 3 - Add a money count variable and a button to increase it

We create a global variable and write code to update the web page with it's value in the redraw_screen() function.

````
  var money_count      = 10;
````

## Goal 4 - Add an Income Producing Asset

# Next Stages (Coming Soon)

* Creating multiple assets
* Adding a graph
* Adding upgrades
* Recording High Score

