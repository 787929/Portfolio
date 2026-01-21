## Use of Custom Functions & Error Checking/Restrictions

isCollidedUp()
This function took in coordinates, velocities and sizes and returned true or false weather the given coordinates collided with the roof of a block

I implemented it like this because collision with the world is used in multiple different features with their own behavior, so by returning true or false each feature can cut down on the amount of lines used and also carry out their own behavior.

A challenge of implementing collision with the world is it causes it to return false when it is colliding with the edge of a block. To fix this problem I also checked the block collision on the right.

recipe()
this function takes in an ID and sets the global variable of recipe to an integer array

I implemented it like this so code outside of the function can access the recipe and then do their checks. This was mostly implemented for organizational sake because it is not used in any other area than that but it keeps all the code clean.

One challenge I had while making this was finding out how to store the item need and the item amount needed. I solved this by making one slot the id and the next the amount and iterating by 2 while looking through the recipe.

renderAllTiles()
this function renders all of the tiles on screen

I implemented it this way for organization's sake and so it was easy to adjust the layering of the rendering.

[Go Back](/posts/learning_logs.md)
