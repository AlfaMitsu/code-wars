Sum of prime-indexed elements

    package kata
    
    // Helper function to check if a number is prime
    func isPrime(n int) bool {
        if n <= 1 {
            return false
        }
        if n <= 3 {
            return true
        }
        if n%2 == 0 || n%3 == 0 {
            return false
        }
        for i := 5; i*i <= n; i += 6 {
            if n%i == 0 || n%(i+2) == 0 {
                return false
            }
        }
        return true
    }
    
    func Solve(arr []int) int {
        sum := 0
        for i, val := range arr {
            if isPrime(i) {
                sum += val
            }
        }
        return sum
    }
