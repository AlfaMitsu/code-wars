Reverse List

    package kata
    
    func ReverseList(lst []int) []int {
        reversed := make([]int, len(lst))
        for i, j := 0, len(lst)-1; i < len(lst); i, j = i+1, j-1 {
            reversed[i] = lst[j]
        }
        return reversed
    }
