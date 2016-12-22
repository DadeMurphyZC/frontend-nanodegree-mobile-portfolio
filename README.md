## Website Performance Optimization portfolio project

This project includes Critical Rendering Path and Javascript performance optimizations using techniques learned in the Udacity course: [Critical Rendering Path course](https://www.udacity.com/course/ud884).

My finished project can be accessed here:
[https://dademurphyzc.github.io/frontend-nanodegree-mobile-portfolio/](https://dademurphyzc.github.io/frontend-nanodegree-mobile-portfolio/)

### Optimization review

####Part 1: Optimize PageSpeed Insights score for index.html
1. Inline CSS into the Head/Style tag in index.html

2. Update render-blocking javascript with the async property.

3. Optimize image sizes for minimal download and resizing, run compression, and convert images to .png file type.

####Part 2: Optimize Frames per Second in pizza.html
1. Refactor changePizzaSizes() function and move the **i**, **dx**, and **newwidth** variables out of the for loop.
   Keeping them within the function scope allows them to be used in the function call, but taking them out of the loop stops redundant        instances of the variables from being created upon every loop iteration.
   
2. Refactor **Document.queryselectorall()** calls to **Document.getElementsByClassName** and cache the returned values in a variable to eliminate expensive, and repetitive, DOM traversals inside of loops.

3. Refactor **updatePositions()** function and move the **cachedLength** and **top** variables out of the for loop.
   Keeping them within the function scope allows them to be used in the function call, but taking them out of the loop stops redundant        instances of the variables from being created upon every loop iteration.
   
4. Edit the anonymous function within the **document.addEventListener()** function, the for loop originally generated 200 pizzas, changed the number to 32. Also updated the **document.queryselectorall()** call to **document.getElementsById("")** to save time on Document DOM traversal.
