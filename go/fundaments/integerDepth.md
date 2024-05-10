Integer Depth

    package kata
    
    func ComputeDepth(n uint) uint {
        seenDigits := make(map[uint]bool)
        depth := uint(0)
        
        for {
            depth++
            multiple := n * depth
            
            for multiple > 0 {
                digit := multiple % 10
                seenDigits[digit] = true
                multiple /= 10
            }
            
            if len(seenDigits) == 10 {
                break
            }
        }
        
        return depth
    }
