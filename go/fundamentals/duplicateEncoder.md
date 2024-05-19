Duplicate Encoder

    package kata
    
    import "strings"
    
    func DuplicateEncode(word string) string {
        word = strings.ToLower(word)
        result := ""
        for _, char := range word {
            if strings.Count(word, string(char)) > 1 {
                result += ")"
            } else {
                result += "("
            }
        }
        return result
    }
