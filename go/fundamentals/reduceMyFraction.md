Reduce my Fraction

    package kata
    
    // Helper function to compute the GCD of two numbers using the Euclidean algorithm
    func gcd(a, b int) int {
        for b != 0 {
            a, b = b, a % b
        }
        return a
    }
    
    // Function to reduce the fraction to its simplest form
    func ReduceFraction(fraction [2]int) [2]int {
        numerator, denominator := fraction[0], fraction[1]
        divisor := gcd(numerator, denominator)
        return [2]int{numerator / divisor, denominator / divisor}
    }
