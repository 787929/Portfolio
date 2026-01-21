## Use of Custom Functions & Error Checking/Restrictions

###   try{
###     if(y >= worldHeight * tileSize - l){
###       return true;
###     }
###     else if((isCollided(x + 1, y + l, w - 2, 0, worldX * tileSize, (worldY + 1) * tileSize, tileSize, vy) && tileHasCollision[(worldY + 1) * worldWidth + worldX]) || 
###     (isCollided(x + 1, y + l, w - 2, 0, (worldX + 1) * tileSize, (worldY + 1) * tileSize, tileSize, vy) && tileHasCollision[(worldY + 1) * worldWidth + worldX + 1])) return true;
###     else return false;
###   }

isCollidedUp()
This function took in coordinates, velocities and sizes and returned true or false weather the given coordinates collided with the roof of a block

I implemented it like this because collision with the world is used in multiple different features with their own behavior, so by returning true or false each feature can cut down on the amount of lines used and also carry out their own behavior.

A challenge of implementing collision with the world is it causes it to return false when it is colliding with the edge of a block. To fix this problem I also checked the block collision on the right.

### void recipe(int ID){
###   recipe = new int[0];
###   if(ID == 1) recipe =  new int[]{2, 3, 5, 2}; 
###   else if(ID == 0) recipe =  new int[]{2, 5, 200, 1, 5, 1, 1, 5}; 
###   else if(ID == 2) recipe =  new int[]{200, 1, 2, 2}; 

recipe()
this function takes in an ID and sets the global variable of recipe to an integer array

I implemented it like this so code outside of the function can access the recipe and then do their checks. This was mostly implemented for organizational sake because it is not used in any other area than that but it keeps all the code clean.

One challenge I had while making this was finding out how to store the item need and the item amount needed. I solved this by making one slot the id and the next the amount and iterating by 2 while looking through the recipe.

### for(int i = 0; i < tileID.length; i++){
###   if(isCollided(i % worldWidth * tileSize + offsetX, int(i / worldWidth) * tileSize + offsetY, tileSize, tileSize, 0, 0, width, height)){
###     if(tileID[i] == 0){
###       fill(100, 175, 255);
###       square(i % worldWidth * tileSize + offsetX, int(i / worldWidth) * tileSize + offsetY, tileSize);
###     }
###     else if(tileID[i] == 1) image(dirt, i % worldWidth * tileSize + offsetX, int(i / worldWidth) * tileSize + offsetY);
###     else if(tileID[i] == 2) image(amber, i % worldWidth * tileSize + offsetX, int(i / worldWidth) * tileSize + offsetY);

renderAllTiles()
this function renders all of the tiles on screen

I implemented it this way for organization's sake and so it was easy to adjust the layering of the rendering.

[Go Back](/posts/learning_logs.md)
