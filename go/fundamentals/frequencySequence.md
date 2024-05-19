Frequency Sequence

    package kata
    
    import "strconv"
    
    func FreqSeq(str string, sep string) string {
        freq := make(map[rune]int)
        
        // Count the frequency of each character
        for _, char := range str {
            freq[char]++
        }
        
        // Construct the output string
        var result string
        for _, char := range str {
            result += strconv.Itoa(freq[char]) + sep
        }
        
        // Remove the trailing separator
        if len(result) > 0 {
            result = result[:len(result)-len(sep)]
        }
        
        return result
    }
