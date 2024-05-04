Merge 2 sorted arrays into 1

    package kata
    
    import "sort"
    
    func MergeArrays(arr1, arr2 []int) []int {
        merged := append(arr1, arr2...)
        sort.Ints(merged)
    
        uniqueMerged := []int{}
        for i := 0; i < len(merged); i++ {
            if i == 0 || merged[i] != merged[i-1] {
                uniqueMerged = append(uniqueMerged, merged[i])
            }
        }
        return uniqueMerged
    }
