Enumerable Magic #20 Cascading Subsets

    package kata
    
    func EachCons(arr []int, n int) [][]int {
        result := [][]int{}
        for i := 0; i <= len(arr)-n; i++ {
            subset := arr[i : i+n]
            result = append(result, subset)
        }
        return result
    }
