Pentabonacci

    package kata
    
    func CountOddPentaFib(n int) int {
        if n < 0 {
            return 0
        }
    
        // Initial terms of the Pentanacci sequence
        pentaFib := []int{0, 1, 1, 2, 4}
        
        // A set to store unique odd terms
        oddTerms := make(map[int]struct{})
    
        // Pre-fill the initial odd terms
        if n >= 1 {
            oddTerms[1] = struct{}{}
        }
    
        // Generate Pentanacci sequence up to the n-th term
        for i := 5; i <= n; i++ {
            nextTerm := pentaFib[i-1] + pentaFib[i-2] + pentaFib[i-3] + pentaFib[i-4] + pentaFib[i-5]
            pentaFib = append(pentaFib, nextTerm)
    
            // Check if the term is odd and add to the set if it is
            if nextTerm%2 != 0 {
                oddTerms[nextTerm] = struct{}{}
            }
        }
    
        // Return the number of unique odd terms
        return len(oddTerms)
    }
