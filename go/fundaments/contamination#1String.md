Contamination #1 String

    package kata
    
    import "strings"
    
    func Contamination(text, char string) string {
        if text == "" || char == "" {
            return ""
        }
        return strings.Repeat(char, len(text))
    }
