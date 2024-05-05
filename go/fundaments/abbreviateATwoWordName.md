Abbreviate a Two Word Name

    package kata
    
    import (
        "strings"
        "unicode"
    )
    
    func AbbrevName(name string) string {
        parts := strings.Split(name, " ")
        if len(parts) != 2 {
            return ""
        }
        initials := ""
        for _, part := range parts {
            if len(part) > 0 {
                initials += string(unicode.ToUpper(rune(part[0]))) + "."
            }
        }
        return strings.TrimSuffix(initials, ".")
    }
