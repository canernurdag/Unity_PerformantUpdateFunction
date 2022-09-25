# Performant Update Function

Sometimes, it is better not to call "Update Function" in each frame, unless it changes the feeling.
Let me give some in real life examples: 
- Expensive math caluclations like distance check
- Linq
- Navmesh agent's SetDestination() function
- Network etc

Therefore, it is a good practice to add some duration between "Update Function" calls.

Besides, in some cases, there are several this type expensive "Update Fnctions" which are using "Duration". 
It is another good practice is that starting them in different frames. 
So, we will be able to distribute the load to frames. 

PS: Please note that do not update same type objects individually. 
Instead, using a controller class that has an array or a list to iterate them in "Update Function" is better in terms of performance.
