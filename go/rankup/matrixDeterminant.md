Matrix Determinant

    package kata
    
    func Determinant(matrix [][]int) int {
        size := len(matrix)
        if size == 1 {
            return matrix[0][0]
        }
        if size == 2 {
            return matrix[0][0]*matrix[1][1] - matrix[0][1]*matrix[1][0]
        }
    
        det := 0
        for i := 0; i < size; i++ {
            minor := make([][]int, size-1)
            for j := 0; j < size-1; j++ {
                minor[j] = make([]int, size-1)
            }
    
            for j := 1; j < size; j++ {
                for k := 0; k < size; k++ {
                    if k < i {
                        minor[j-1][k] = matrix[j][k]
                    } else if k > i {
                        minor[j-1][k-1] = matrix[j][k]
                    }
                }
            }
    
            sign := 1
            if i%2 == 1 {
                sign = -1
            }
    
            det += sign * matrix[0][i] * Determinant(minor)
        }
    
        return det
    }
