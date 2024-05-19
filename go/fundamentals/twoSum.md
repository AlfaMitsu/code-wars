Two Sum

    package kata
    
    func TwoSum(numbers []int, target int) [2]int {
        // Create a map to store the indices of numbers
        indexMap := make(map[int]int)
    
        // Iterate through the numbers
        for i, num := range numbers {
            // Calculate the complement needed to reach the target
            complement := target - num
            // Check if the complement exists in the map
            if j, ok := indexMap[complement]; ok {
                // Return the indices if found
                return [2]int{j, i}
            }
            // Store the current number's index in the map
            indexMap[num] = i
        }
    
        // Return an empty array if no solution is found
        return [2]int{}
    }
