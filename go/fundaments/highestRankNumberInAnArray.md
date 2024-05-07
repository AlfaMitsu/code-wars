Highest rank number in an array

    package kata
    
    func HighestRank(nums []int) int {
        // Create a map to store the count of each number
        countMap := make(map[int]int)
    
        // Iterate through the numbers and count their occurrences
        for _, num := range nums {
            countMap[num]++
        }
    
        // Initialize variables to store the highest frequency and the number with that frequency
        highestFreq := 0
        result := 0
    
        // Iterate through the count map to find the number with the highest frequency
        for num, freq := range countMap {
            if freq > highestFreq || (freq == highestFreq && num > result) {
                highestFreq = freq
                result = num
            }
        }
    
        return result
    }
