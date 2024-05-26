Sudoku Solver

    function sudoku(puzzle) {
        function isValid(num, row, col) {
            for (let i = 0; i < 9; i++) {
                if (puzzle[row][i] === num || puzzle[i][col] === num || puzzle[Math.floor(row / 3) * 3 + Math.floor(i / 3)][Math.floor(col / 3) * 3 + i % 3] === num) {
                    return false;
                }
            }
            return true;
        }
    
        function solve() {
            for (let row = 0; row < 9; row++) {
                for (let col = 0; col < 9; col++) {
                    if (puzzle[row][col] === 0) {
                        for (let num = 1; num <= 9; num++) {
                            if (isValid(num, row, col)) {
                                puzzle[row][col] = num;
                                if (solve()) {
                                    return true;
                                }
                                puzzle[row][col] = 0;
                            }
                        }
                        return false;
                    }
                }
            }
            return true;
        }
    
        solve();
        return puzzle;
    }
    
    // Test case
    var puzzle = [
        [5,3,0,0,7,0,0,0,0],
        [6,0,0,1,9,5,0,0,0],
        [0,9,8,0,0,0,0,6,0],
        [8,0,0,0,6,0,0,0,3],
        [4,0,0,8,0,3,0,0,1],
        [7,0,0,0,2,0,0,0,6],
        [0,6,0,0,0,0,2,8,0],
        [0,0,0,4,1,9,0,0,5],
        [0,0,0,0,8,0,0,7,9]
    ];
    
    console.log(sudoku(puzzle));
