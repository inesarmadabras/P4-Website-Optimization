#Website Performance Optimization project
Fourth project from the Front-End Web Developer Nanodegree in Udacity: optimized index.html to achieve a score of 90 in PageSpeed, and optimized main.js to achieve 60 fps in pizza.html.

## 1. Portfolio Optimization
optimized index.html to achieve a score of 90 in PageSpeed Insights

###How to run?
Portfolio - https://inesarmadabras.github.io/P4-Website-Optimization/dist/

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

## 2. Portfolio Optimization
Optimized main.js to achieve 60 fps in pizza.html

###How to run?
Portfolio - https://inesarmadabras.github.io/P4-Website-Optimization/dist/

### Optimization for pizza.html
* Apply optimizations for PageSpeed: minify css and js, optimize images, inline css
    - (Result: D: 30/100 to D: **91/100** )

### Optimization for main.js
**Note: all the changes in the code are marked with** `//optimezed`

`l.196 - l.272` - The  default case (scifi) at ```function getNoun()``` and scientific at ```function getAdj()``` as been optimized

`l.442` - created ```var pizzaContainers```.Now, pizzaContainers is out of the for loop

`l.498` - function ```changePizzaSizes()``` optimized with a simplified for cycle

`l.496` - Sliding background pizzas optimized (with https://www.html5rocks.com/en/tutorials/speed/animations/)  

`l.515` - ```updatePositions()``` optimized

---------
## 3. Extras: 
* All the code was been validated with https://validator.w3.org/ and http://jshint.com/
