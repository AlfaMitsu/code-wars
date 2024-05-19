Love VS Friendship

    package kata
    
    func WordsToMarks(s string) int {
        sum := 0
        for _, char := range s {
            // Convert lowercase character to its position in the alphabet
            // ASCII 'a' is 97, so subtract 96 to get position in the alphabet
            sum += int(char) - 96
        }
        return sum
    }
