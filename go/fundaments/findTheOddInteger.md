Find the odd Integer

    package kata
    
    func FindOdd(seq []int) int {
        counts := make(map[int]int)
        for _, num := range seq {
            counts[num]++
        }
        for num, count := range counts {
            if count%2 != 0 {
                return num
            }
        }
        return -1 // Error: No number found
    }
