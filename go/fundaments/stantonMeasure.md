Stanton Measure

    package kata
    
    func StantonMeasure(arr []int) int {
        count := 0
        for _, num := range arr {
            if num == 1 {
                count++
            }
        }
    
        stantonCount := 0
        for _, num := range arr {
            if num == count {
                stantonCount++
            }
        }
    
        return stantonCount
    }
