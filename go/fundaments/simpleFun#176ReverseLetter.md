Simple Fun #176: Reverse Letter

    package kata
    
    func ReverseLetters(s string) string {
        var result string
        for i := len(s) - 1; i >= 0; i-- {
            if isAlphabetic(s[i]) {
                result += string(s[i])
            }
        }
        return result
    }
    
    func isAlphabetic(c byte) bool {
        return (c >= 'a' && c <= 'z') || (c >= 'A' && c <= 'Z')
    }
