Array Diff

    package kata
    
    func ArrayDiff(a, b []int) []int {
        // Create a map to store the values in b for quick lookup
        bMap := make(map[int]struct{})
        for _, val := range b {
            bMap[val] = struct{}{}
        }
    
        // Create a result slice to store the values not present in b
        result := []int{}
        for _, val := range a {
            if _, found := bMap[val]; !found {
                result = append(result, val)
            }
        }
    
        return result
    }
