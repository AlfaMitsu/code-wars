Expression Matter

    package kata
    
    func max(a, b int) int {
        if a > b {
            return a
        }
        return b
    }
    
    func ExpressionMatter(a int, b int, c int) int {
        maxVal := 0
        maxVal = max(maxVal, a+b+c)
        maxVal = max(maxVal, a*b*c)
        maxVal = max(maxVal, a+b*c)
        maxVal = max(maxVal, a*b+c)
        maxVal = max(maxVal, (a+b)*c)
        maxVal = max(maxVal, a*(b+c))
        
        return maxVal
    }
