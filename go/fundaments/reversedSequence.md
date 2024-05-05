Reversed sequence

    package kata
    
    func ReverseSeq(n int) []int {
        result := make([]int, 0, n)
        for i := n; i > 0; i-- {
            result = append(result, i)
        }
        return result
    }
