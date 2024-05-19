What dominates your array?

    package kata
    
    func Dominator(a []int) int {
        counts := make(map[int]int)
        
        // Count occurrences of each element
        for _, num := range a {
            counts[num]++
        }
        
        // Find the element with count > len(a)/2
        for num, count := range counts {
            if count > len(a)/2 {
                return num
            }
        }
        
        return -1
    }
