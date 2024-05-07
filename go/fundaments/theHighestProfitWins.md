The Highest Profit Wins

    package kata
    
    import "sort"
    
    func MinMax(arr []int) [2]int {
        sort.Ints(arr)
        return [2]int{arr[0], arr[len(arr)-1]}
    }
