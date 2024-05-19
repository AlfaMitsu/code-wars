Consecutive K-Primes

    package kata
    
    // Helper function to count the number of prime factors of a number
    func countPrimeFactors(n int) int {
        count := 0
        factor := 2
        
        for n > 1 {
            if n % factor == 0 {
                count++
                n /= factor
                // Keep counting the same factor if it's a factor multiple times
                for n % factor == 0 {
                    n /= factor
                    count++
                }
            }
            factor++
        }
        
        return count
    }
    
    // Main function to count consecutive k-primes in the list
    func ConsecKprimes(k int, arr []int) int {
        count := 0
        
        for i := 0; i < len(arr) - 1; i++ {
            if countPrimeFactors(arr[i]) == k && countPrimeFactors(arr[i+1]) == k {
                count++
            }
        }
        
        return count
    }
