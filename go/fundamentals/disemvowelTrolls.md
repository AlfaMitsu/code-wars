Disemvowel Trolls

    package kata
    
    import "strings"
    
    func Disemvowel(comment string) string {
        vowels := "aeiouAEIOU"
        result := strings.Builder{}
        for _, char := range comment {
            if !strings.ContainsRune(vowels, char) {
                result.WriteRune(char)
            }
        }
        return result.String()
    }
