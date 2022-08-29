# PacMan Project
## A repository for a coding assignment through MIT | xPro for their <br> Professional Certificate in Coding: Full Stack Development with MERN program.

### Goal:
The goal of this project was to take alternating images of the character PacMan and to have him move across the screen. Further, we also needed to determine how to have the image and direction reverse once the character hit the edge of the screen.

### Execution:
Much of the code for PacMan was provided at the start. The combination of four images was set up in an array. We also had predetermined global variables for PacMan's position (var pos), the direction PacMan was moving (var direction), and the way PacMan was facing (var focus). Both direction and focus alternate between 0 and 1 once the code is completed. We also had a function pre-made (Run) which would move PacMan forward upon a mouse click. We also had an incomplete function, checkPageBounds(direction, imgWidth).

What ultimately needed to be added in order for the code to work properly was the following. First, a new global variable had to be introduced, var pageWidth = window.innerWidth. This variable was added as an additional argument for both the Run and checkPageBounds functions. Further, the global variable of pos was also added to checkPageBounds.

Regarding the functionality of checkPageBounds, the outcome was that the function needed to check two conditions. If direction was 0 and both the position and the width of PacMan did not exceed the width of the page, PacMan would change directions (direction would equal 1). If direction was 1 and if the position of PacMan was less than 0, direction would flip back to 0. The function would end by returning the value of direction.

With the boundaries set, PacMan would move across the sceen automatically by adding the setInterval function to the code. This parameters would be the Run function and 200 mileseconds.
