Jaden Casing Strings

    package kata
    
    import "strings"
    
    func ToJadenCase(str string) string {
        words := strings.Split(str, " ")
        for i, word := range words {
            if len(word) > 0 {
                words[i] = strings.ToUpper(string(word[0])) + word[1:]
            }
        }
        return strings.Join(words, " ")
    }
