## Variables & Data Tracking

I used floats for any x, y, vx and vy values to allow for a more resilient to decimals as there will be division and multiplication which can return a decimal.
The First way I used integers for IDs as it would never be a decimal, it is also easier to pick up the ID system as it all is whole numbers that follow a theme.
The second way I used integers for amounts and timers as they are easier to work with and they also will never be a decimal.
The third way I used integers is to increase readability and to allow for easier adjustments.
I used boolean values to toggle on and off properties and controls because a toggle will always be on or off and using boolean allows for easier implementation into if statement.

Problems I had with variables and data tracking is it was difficult to store all the properties of all the arrays. The way I came around this is by making multiple boolean arrays and making a spawn function that takes the ID and sets the properties of that block to what a block with that ID would have.

[Go Back](/posts/learning_logs.md)
