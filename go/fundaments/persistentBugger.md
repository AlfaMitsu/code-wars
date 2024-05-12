Persistent Bugger

    package kata
    
    import "strconv"
    
    func Persistence(n int) int {
        count := 0
    
        for n >= 10 {
            product := 1
            digits := strconv.Itoa(n)
            for _, digit := range digits {
                num, _ := strconv.Atoi(string(digit))
                product *= num
            }
            n = product
            count++
        }
    
        return count
    }
