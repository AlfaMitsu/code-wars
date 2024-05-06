VAPORCODE

    package kata
    
    import (
        "bytes"
        "unicode"
    )
    
    func Vaporcode(s string) string {
        var buf bytes.Buffer
        for _, r := range s {
            if !unicode.IsSpace(r) {
                buf.WriteString(string(unicode.ToUpper(r)))
                buf.WriteString("  ")
            }
        }
        return buf.String()[:len(buf.String())-2]
    }
