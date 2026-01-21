## Arrays & Data Structures

### int[] itemIsPlaceable = new int[]{1, 3, 4, 6, 8, 9, 10, 12, 13, 14, 15, 16};
### int[] itemIsWeapon = new int[]{101, 104, 107, 110};
### int[] itemIsAmulet = new int[]{102, 105, 108, 111};

### int[] itemID = new int[50];
### int[] itemAmount = new int[50];
### int[] itemDeathTimer = new int[50];

I used arrays to iterate through multiple values which allows for a scalable amount of projectiles, items, etc.
I also used arrays to have a set list of properties that correlate to an ID. This is a really useful and organized way of collecting properties but it was not used often as it did not work well with the existing ID system.

One problem is properties for arrays were loaded when they were spawned, but the items in the inventory were not spawned but still had properties. to fix this what I did is create an array of IDs and the properties were given there. That means it allowed me to find the properties of that ID instead of finding the properties of that item.

[Go Back](/posts/learning_logs.md)
