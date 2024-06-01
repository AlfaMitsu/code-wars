Take a ten minutes walk

    function isValidWalk(walk) {
      // Check if the walk takes exactly 10 minutes
      if (walk.length !== 10) return false;
    
      // Initialize starting coordinates
      let x = 0, y = 0;
    
      // Process each direction in the walk
      for (let direction of walk) {
        switch (direction) {
          case 'n':
            y += 1;
            break;
          case 's':
            y -= 1;
            break;
          case 'e':
            x += 1;
            break;
          case 'w':
            x -= 1;
            break;
        }
      }
    
      // Check if we are back at the starting point
      return x === 0 && y === 0;
    }
    
    // Example usage:
    console.log(isValidWalk(['n','s','n','s','n','s','n','s','n','s'])); // true
    console.log(isValidWalk(['w','e','w','e','w','e','w','e','w','e','w','e'])); // false
    console.log(isValidWalk(['w'])); // false
    console.log(isValidWalk(['n','n','n','s','n','s','n','s','n','s'])); // false
