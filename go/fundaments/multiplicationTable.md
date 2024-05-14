Multiplication Table

    package multiplicationtable
    
    func MultiplicationTable(size int) [][]int {
        table := make([][]int, size)
        for i := 0; i < size; i++ {
            table[i] = make([]int, size)
            for j := 0; j < size; j++ {
                table[i][j] = (i + 1) * (j + 1)
            }
        }
        return table
    }
