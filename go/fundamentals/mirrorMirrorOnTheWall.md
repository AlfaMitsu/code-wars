Mirror Mirror on the Wall

    package kata
    
    import "sort"
    
    func Mirror(data []int) []int {
        // Sort the input array
        sorted := make([]int, len(data))
        copy(sorted, data)
        sort.Ints(sorted)
    
        // Create the mirrored array with correct length
        mirroredLen := len(data)*2 - 1
        if mirroredLen < 0 {
            mirroredLen = 0
        }
        mirrored := make([]int, mirroredLen)
        for i, num := range sorted {
            mirrored[i] = num
            mirrored[mirroredLen-1-i] = num
        }
    
        return mirrored
    }
