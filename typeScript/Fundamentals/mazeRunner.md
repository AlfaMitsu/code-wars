Maze Runner

    export function mazeRunner(maze: number[][], directions: string[]): string {
        let x = 0;
        let y = 0;
    
        // Find the start position
        for (let i = 0; i < maze.length; i++) {
            for (let j = 0; j < maze[i].length; j++) {
                if (maze[i][j] === 2) {
                    x = i;
                    y = j;
                    break;
                }
            }
        }
    
        // Follow the directions
        for (let i = 0; i < directions.length; i++) {
            switch (directions[i]) {
                case "N":
                    x--;
                    break;
                case "S":
                    x++;
                    break;
                case "E":
                    y++;
                    break;
                case "W":
                    y--;
                    break;
            }
    
            // Check if out of bounds
            if (x < 0 || y < 0 || x >= maze.length || y >= maze[x].length) {
                return "Dead";
            }
    
            // Check if hit a wall
            if (maze[x][y] === 1) {
                return "Dead";
            }
    
            // Check if reached finish
            if (maze[x][y] === 3) {
                return "Finish";
            }
        }
    
        // Check if lost
        return "Lost";
    }
