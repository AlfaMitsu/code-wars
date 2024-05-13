Scrabble Score

    package kata
    
    import "unicode"
    
    func ScrabbleScore(st string) int {
        // Define the letter values
        letterValues := map[rune]int{
            'A': 1, 'E': 1, 'I': 1, 'O': 1, 'U': 1, 'L': 1, 'N': 1, 'R': 1, 'S': 1, 'T': 1,
            'D': 2, 'G': 2,
            'B': 3, 'C': 3, 'M': 3, 'P': 3,
            'F': 4, 'H': 4, 'V': 4, 'W': 4, 'Y': 4,
            'K': 5,
            'J': 8, 'X': 8,
            'Q': 10, 'Z': 10,
        }
    
        // Initialize the score
        score := 0
    
        // Calculate the score for each letter in the input string
        for _, char := range st {
            // Convert the letter to uppercase
            char = unicode.ToUpper(char)
            // Check if the letter is in the letterValues map
            if value, ok := letterValues[char]; ok {
                score += value
            }
        }
    
        return score
    }
