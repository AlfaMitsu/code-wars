Battleship Field Validator

    function validateBattlefield(field) {
      const SHIP_COUNTS = { 1: 4, 2: 3, 3: 2, 4: 1 };
      let shipsFound = { 1: 0, 2: 0, 3: 0, 4: 0 };
    
      // Direction vectors for 8 possible neighbors
      const neighbors = [
        [-1, -1], [-1, 0], [-1, 1],
        [0, -1],          [0, 1],
        [1, -1], [1, 0], [1, 1]
      ];
    
      const inBounds = (x, y) => x >= 0 && y >= 0 && x < 10 && y < 10;
    
      // DFS to find and mark a ship
      function dfs(x, y) {
        const stack = [[x, y]];
        const cells = [];
        while (stack.length) {
          const [cx, cy] = stack.pop();
          if (!inBounds(cx, cy) || field[cx][cy] === 0) continue;
          cells.push([cx, cy]);
          field[cx][cy] = 0; // Mark as visited
          for (const [dx, dy] of neighbors) {
            const nx = cx + dx;
            const ny = cy + dy;
            if (inBounds(nx, ny) && field[nx][ny] === 1) {
              stack.push([nx, ny]);
            }
          }
        }
        return cells;
      }
    
      // Check if cells form a valid ship
      function isValidShip(cells) {
        if (cells.length === 1) return true; // Submarine
        let xs = new Set(), ys = new Set();
        for (const [x, y] of cells) {
          xs.add(x);
          ys.add(y);
        }
        return xs.size === 1 || ys.size === 1;
      }
    
      // Ensure no neighboring ships
      function noContact(cells) {
        for (const [x, y] of cells) {
          for (const [dx, dy] of neighbors) {
            const nx = x + dx;
            const ny = y + dy;
            if (inBounds(nx, ny) && field[nx][ny] === 1) {
              return false;
            }
          }
        }
        return true;
      }
    
      // Traverse the grid to find ships
      for (let i = 0; i < 10; i++) {
        for (let j = 0; j < 10; j++) {
          if (field[i][j] === 1) {
            const cells = dfs(i, j);
            if (!isValidShip(cells) || !noContact(cells)) {
              return false;
            }
            const size = cells.length;
            if (size < 1 || size > 4) return false;
            shipsFound[size]++;
          }
        }
      }
    
      // Check if the number of ships is correct
      for (const size in SHIP_COUNTS) {
        if (shipsFound[size] !== SHIP_COUNTS[size]) {
          return false;
        }
      }
    
      return true;
    }
