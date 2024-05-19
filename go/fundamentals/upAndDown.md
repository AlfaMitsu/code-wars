Up and Down

    package kata
    
    import (
        "strings"
    )
    
    func Arrange(s string) string {
        words := strings.Fields(s)
        n := len(words)
        
        for i := 0; i < n-1; i++ {
            if i%2 == 0 && len(words[i]) > len(words[i+1]) {
                words[i], words[i+1] = words[i+1], words[i]
            } else if i%2 != 0 && len(words[i]) < len(words[i+1]) {
                words[i], words[i+1] = words[i+1], words[i]
            }
        }
        
        result := ""
        for i, word := range words {
            if i%2 == 0 {
                result += strings.ToLower(word)
            } else {
                result += strings.ToUpper(word)
            }
            if i < len(words)-1 {
                result += " "
            }
        }
        
        return result
    }
