The Supermarket Queue

    package kata
    
    
    func QueueTime(customers []int, n int) int {
        if len(customers) == 0 {
            return 0
        }
        
        tills := make([]int, n)
        for _, c := range customers {
            minIndex, minValue := 0, tills[0]
            for i, v := range tills {
                if v < minValue {
                    minIndex, minValue = i, v
                }
            }
            tills[minIndex] += c
        }
        
        max := tills[0]
        for _, v := range tills {
            if v > max {
                max = v
            }
        }
        
        return max
    }
