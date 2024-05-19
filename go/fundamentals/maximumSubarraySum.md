Maximum Subarray Sum

    package kata
    
    func MaximumSubarraySum(numbers []int) int {
        maxEndingHere := 0
        maxSoFar := 0
    
        for _, num := range numbers {
            maxEndingHere = max(num, maxEndingHere+num)
            maxSoFar = max(maxSoFar, maxEndingHere)
        }
    
        return maxSoFar
    }
    
    func max(a, b int) int {
        if a > b {
            return a
        }
        return b
    }
