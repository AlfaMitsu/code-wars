Sorting by Bits

    package kata
    
    import (
        "sort"
    )
    
    // Function to count the number of 1 bits in the binary representation of an integer
    func countBits(n int) int {
        count := 0
        for n != 0 {
            count += n & 1
            n >>= 1
        }
        return count
    }
    
    // Function to sort the array based on the number of 1 bits
    func SortByBit(arr []int) {
        sort.Slice(arr, func(i, j int) bool {
            countI := countBits(arr[i])
            countJ := countBits(arr[j])
            if countI == countJ {
                return arr[i] < arr[j]
            }
            return countI < countJ
        })
    }
