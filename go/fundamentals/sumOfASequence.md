Sum of a sequence

    package kata
    
    func SequenceSum(start, end, step int) int {
        if start > end {
            return 0
        }
        
        sum := 0
        for i := start; i <= end; i += step {
            sum += i
        }
        
        return sum
    }
