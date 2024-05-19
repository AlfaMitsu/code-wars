Counting Sheep

    package kata
    
    func CountSheeps(numbers []bool) int {
        count := 0
        for _, present := range numbers {
            if present {
                count++
            }
        }
        return count
    }
