Odd-Even String Sort

    package kata
    
    import "strings"
    
    func SortMyString(s string) string {
        var evenChars, oddChars []string
        for i, char := range s {
            if i%2 == 0 {
                evenChars = append(evenChars, string(char))
            } else {
                oddChars = append(oddChars, string(char))
            }
        }
        return strings.Join([]string{strings.Join(evenChars, ""), strings.Join(oddChars, "")}, " ")
    }
