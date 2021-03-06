#Website Performance Optimization project 
##Front-End Web Developer Nanodegree - Udacity - [Check the Project Review](https://review.udacity.com/#!/reviews/260974/shared)

Fourth project from the Front-End Web Developer Nanodegree in Udacity: Optimized an inefficient web application's JavaScript, CSS and assets delivery, ensuring it runs at 60fps and achieves a PageSpeed score of at least 90.

## 1. Portfolio Optimization
optimized index.html to achieve a score of 90 in PageSpeed Insights

###How to run?
* **Optimized Portfolio** -  https://inesarmadabras.github.io/P4-Website-Optimization/dist/
* Original Portfolio - https://inesarmadabras.github.io/P4-Website-Optimization/original/

##PageSpeed Insights: 
* Link: [PageSpeed Insights Result](https://goo.gl/h86ReC) 
    - **Mobile: 93/100    Desktop: 95/100**
    - Original - Mobile: 27/100  Desktop: 29/100

###Optimization for the index.html

* Eliminate render-blocking JS and CSS:
    - I inlined and minifyed the entire `style.css` and some of the `.js` to `index.html`.
    - print.css with  the media="print" tag
    - All the js scripts are marked async, making sure they will not blocking the parsing.

* Loaded Google Fonts with the Web Font Loader
(https://developers.google.com/fonts/docs/webfont_loader)

* I resized pizzeria to 100px width with a strong compression rate.

* I optimized all the pics with [Optimizilla](http://optimizilla.com/)  

* I created minimized versions of all css and js files 
(with Minify, a [Sublime Text plugin](https://packagecontrol.io/packages/Minify)

* Cache Optimization:
    - Create web.config file to put an expiry date to static resources (css, images and js).

* Put the Google Analytics script at the footer of the page.

## 2. Code Optimization
Optimized main.js to achieve 60 fps in pizza.html

###How to run?
* **Optimized pizza page** - https://inesarmadabras.github.io/P4-Website-Optimization/dist/views/pizza.html
* Original pizza page - https://inesarmadabras.github.io/P4-Website-Optimization/original/views/pizza.html

### Optimization for pizza.html
* Apply optimizations for PageSpeed: minify css and js, optimize images, inline css
    - (Result: D: 30/100 to D: **91/100** )

### Optimization for main.js
**Note: all the changes in the code are marked with** `//optimezed`

`l.196 - l.272` - The  default case (scifi) at ```function getNoun()``` and scientific at ```function getAdj()``` as been optimized

`l.442` - created ```var pizzaContainers```.Now, pizzaContainers is out of the for loop

`l.498` - function ```changePizzaSizes()``` optimized with a simplified for cycle

`l.496` - Sliding background pizzas optimized (with https://www.html5rocks.com/en/tutorials/speed/animations/)  

`l.482` `var pizzaDiv` declared outside of the for cycle

`l.515` - ```updatePositions()``` optimized


#### Updates (new submission):
Changed ```querySelector``` calls to `getElementById`

`l.468` - definition of ```pizzaDiv``` variable is now out of for loop.

`l.556` - definition of ```movingPizzas``` variable is now out of for loop.

`l.517` - ```function updatePositions()``` redone: new array ```var phases[]```



---------
## 3. Extras: 
* All the code was been validated with https://validator.w3.org/ and http://jshint.com/

## Update (8/11/2016):
* Added comments: Header comment, Function Header 
* `l.572` `var elem` declared outside of the `for` cycle
