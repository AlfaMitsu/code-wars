Convert number to reversed array of digits
    
    package kata
    
    func Digitize(n int) []int {
        if n == 0 {
            return []int{0}
        }
    
        result := []int{}
        for n > 0 {
            digit := n % 10
            result = append(result, digit)
            n /= 10
        }
    
        return result
    }
