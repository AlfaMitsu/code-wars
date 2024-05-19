Sort the Vowels!

    package kata
    
    import "strings"
    
    func SortVowels(s string) string {
        if s == "" {
            return ""
        }
    
        vowels := "aeiouAEIOU"
        var result strings.Builder
    
        for _, char := range s {
            if strings.ContainsRune(vowels, char) {
                result.WriteByte('|')
                result.WriteRune(char)
            } else {
                result.WriteRune(char)
                result.WriteByte('|')
            }
            result.WriteByte('\n')
        }
    
        // Remove the extra newline at the end
        return strings.TrimSuffix(result.String(), "\n")
    }
