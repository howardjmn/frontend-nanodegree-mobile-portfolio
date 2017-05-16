## Website Performance Optimization portfolio project

View the main page in your browser [here](https://rawgit.com/howardjmn/frontend-nanodegree-mobile-portfolio/master/index.html).  Click 'Cam's Pizzeria' to view the Pizza page.

## My Solutions

###Part 1: Optimize PageSpeed Insights score for index.html

#### What needs to be done?

1. Identify and perform optimizations to achieve a PageSpeed score above 90 on index.html.

#### What did I do?

1. Prevented render blocking JS by making analytics.js async.
2. Prevented render blocking CSS by using media type "print" to print.css.
3. Optimized style.css delivery by making it inline CSS in index.html.
4. Optimized jpg images using the online tool [Optimizilla](http://optimizilla.com/).


### Part 2: Optimize Frames per Second in pizza.html

#### What needs to be done?

1. Time to resize pizzas is less than 5ms in pizza.html shown in the browser console.
2. Identify and perform optimizations ensuring a consistent frame rate at 60fps when scrolling in pizza.html.

#### What did I do?

PIZZA.HTML:

1. Optimized style.css delivery by making it inline CSS in pizza.html.
2. Optimized pizza.png and pizzeria.jpg using the online tool [Optimizilla](http://optimizilla.com/).
3. Implemented separate non-mobile and mobile (smaller) images.
4. Preload bootstrap grid css file.

MAIN.JS:

1. Function 'changePizzaSizes':
    - moved variable definition and assignment outside of loop
    - replaced querySelectorAll with getElementsByClassName
2. Built 'randomPizza' div using requestAnimationFrame
3. Built 'mover' class with single getElementsByClassName instead of loop with querySelectorAll
4. Function 'updatePositions':
    - moved 'phase' variable definition and assignment outside of loop because it needs to done just once.
5. Reworked the sliding pizza generator using requestAnimationFrame.  Also replaced querySelector with getElementById.