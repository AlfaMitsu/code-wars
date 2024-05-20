Surrounding Primes for a value

    package kata
    
    func PrimeBefAft(n int) [2]int {
        befPrime := largestPrimeBefore(n)
        aftPrime := smallestPrimeAfter(n)
        return [2]int{befPrime, aftPrime}
    }
    
    func largestPrimeBefore(n int) int {
        for i := n - 1; i > 1; i-- {
            if isPrime(i) {
                return i
            }
        }
        return 2 // No prime found, return 2 as the smallest prime
    }
    
    func smallestPrimeAfter(n int) int {
        for i := n + 1; ; i++ {
            if isPrime(i) {
                return i
            }
        }
    }
    
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
