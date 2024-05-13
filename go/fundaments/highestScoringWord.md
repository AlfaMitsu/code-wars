Highest Scoring Word

    package kata
    
    import "strings"
    
    func High(s string) string {
        words := strings.Fields(s)
        maxScore := 0
        highestWord := ""
    
        for _, word := range words {
            score := 0
            for _, char := range word {
                score += int(char) - 'a' + 1
            }
            if score > maxScore {
                maxScore = score
                highestWord = word
            }
        }
    
        return highestWord
    }
