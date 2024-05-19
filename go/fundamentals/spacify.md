Spacify

    package kata
    
    import "strings"
    
    func Spacify(s string) string {
        return strings.Join(strings.Split(s, ""), " ")
    }
