Wilson Primes

    package kata
    
    func AmIWilson(n int) bool {
        // Check if the number is one of the known Wilson primes
        return n == 5 || n == 13 || n == 563
    }
