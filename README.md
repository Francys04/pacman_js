## Pacman Game

- This is a well-structured HTML and Javascript code for a Pacman game. Here's a breakdown of the code:

### HTML Structure:

- The code starts with basic HTML tags to define the document structure and viewport size.
- It links two external Javascript files (ghost.js and pacman.js) likely containing the logic for ghosts and pacman movement.
- It defines a canvas element for rendering the game visuals.
- There are also hidden image elements for the pacman animation and ghost sprites.

### Javascript Code:

1. Game Variables:

- The code sets up various variables for the game state like fps (frames per second), block size, score, number of lives, and ghost count.
- It creates a 2D array named map representing the layout of the walls (1) and empty spaces (0) in the game.

2. Pacman and Ghost Creation:

- Functions createNewPacman and createGhosts are defined to initialize pacman and ghost objects respectively.
- These functions set the initial position, size, speed, and image references for pacman and ghosts.

3. Game Loop:

- The gameLoop function is called repeatedly using setInterval to continuously update and render the game.
- Inside the loop, the update and draw functions are called to handle game logic and visuals.

4. Update Function:

- This function updates the game state by:
- Calling pacman.moveProcess to handle pacman's movement and eating logic.
- Calling updateGhosts to update the ghosts' positions (likely defined in ghost.js).
- Checking for collisions between pacman and ghosts using pacman.checkGhostCollision (from pacman.js).

4. Draw Function:

- This function clears the canvas and redraws all game elements:
- Walls are drawn based on the map array.
- Food items (represented by a square) are drawn at empty spaces in the map.
- The drawGhosts function (likely from ghost.js) is called to draw the ghosts.
- Pacman is drawn using its own function (pacman.draw from pacman.js).
- Score and remaining lives are displayed on the canvas.

5. Ghost Movement:

- A class named Ghost is defined to handle ghost behavior.
- It has properties for position, size, speed, target location, and image data.
- The moveProcess function determines the ghosts' movement:
- It checks if the ghost is within a certain range of pacman.
- It changes the target location to pacman if it's in range.
- It calls changeDirectionIfPossible to choose a direction towards the target.
- It moves the ghost forward based on the chosen direction.
- It checks for collisions with walls and reverses direction if needed.
- The changeDirectionIfPossible function uses a Breadth-First Search (BFS) algorithm to find the shortest path to the target location considering walls as obstacles.

### Pacman Controls:

- The code listens for keyboard events (keydown) and updates pacman's desired direction based on the pressed key (arrow keys or WASD).

###### Overall, this code effectively implements core functionalities of a Pacman game including character movement, collision detection, pathfinding for ghosts, and scorekeeping. The separation between HTML for structure, Javascript for logic, and potentially separate Javascript files for pacman and ghost behavior makes the code well-organized and maintainable.

![sample](sample.jpeg)
![sample1](sample.png)
