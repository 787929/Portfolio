## Selection Structure 

###  if(ID == 1) image(itemDirt, x, y);
###  else if(ID == 2) image(itemAmber, x, y);
###  else if(ID == 3) image(itemDirtBrick, x, y);
###  else if(ID == 4) image(itemDirtBg, x, y);
###  else if(ID == 5) image(stick, x, y);

I used a selection structure to correlate IDs to properties so spawning a tile would automatically store the properties of that tile in the arrays.

One problem I had with this is it increased the amount of calculations majorly so I made them all else if statements so it doesn't have to check the rest of the IDs if it already found one.

[Go Back](/posts/learning_logs.md)
