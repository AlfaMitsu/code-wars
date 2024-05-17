Integers: Recreation 1

    package kata
    
    import (
        "math"
    )
    
    func ListSquared(m, n int) [][]int {
        result := [][]int{}
        
        for i := m; i <= n; i++ {
            sumSquares := sumOfSquaredDivisors(i)
            if isPerfectSquare(sumSquares) {
                result = append(result, []int{i, sumSquares})
            }
        }
        
        return result
    }
    
    // Helper function to find the sum of squared divisors of a number
    func sumOfSquaredDivisors(num int) int {
        sum := 0
        for i := 1; i <= int(math.Sqrt(float64(num))); i++ {
            if num % i == 0 {
                sum += i * i
                if i != num / i {
                    sum += (num / i) * (num / i)
                }
            }
        }
        return sum
    }
    
    // Helper function to check if a number is a perfect square
    func isPerfectSquare(num int) bool {
        sqrt := int(math.Sqrt(float64(num)))
        return sqrt * sqrt == num
    }
