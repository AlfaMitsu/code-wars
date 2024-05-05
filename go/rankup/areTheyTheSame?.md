Are they the "same"?

    package kata
    
    import (
        "sort"
    )
    
    func Comp(array1 []int, array2 []int) bool {
        if array1 == nil || array2 == nil || len(array1) != len(array2) {
            return false
        }
    
        // Square all elements in array1
        for i, num := range array1 {
            array1[i] = num * num
        }
    
        // Sort both arrays
        sort.Ints(array1)
        sort.Ints(array2)
    
        // Compare the sorted arrays
        for i := range array1 {
            if array1[i] != array2[i] {
                return false
            }
        }
    
        return true
    }
