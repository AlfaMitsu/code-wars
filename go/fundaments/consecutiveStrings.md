Consecutive Strings

    package kata
    
    func LongestConsec(strarr []string, k int) string {
        n := len(strarr)
        if n == 0 || k > n || k <= 0 {
            return ""
        }
    
        var longest string
        for i := 0; i <= n-k; i++ {
            current := ""
            for j := i; j < i+k; j++ {
                current += strarr[j]
            }
            if len(current) > len(longest) {
                longest = current
            }
        }
        return longest
    }
