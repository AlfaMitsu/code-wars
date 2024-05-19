Indexed Capitalization

    package kata
    
    import "unicode"
    
    func Capitalize(st string, arr []int) string {
        runes := []rune(st)
        
        for _, index := range arr {
            if index >= 0 && index < len(runes) {
                runes[index] = unicode.ToUpper(runes[index])
            }
        }
        
        return string(runes)
    }
