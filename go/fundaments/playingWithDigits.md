Playing with digits

    package kata
    
    import "strconv"
    
    func DigPow(n, p int) int {
        sum := 0
        sn := strconv.Itoa(n)
        for _, digit := range sn {
            digitVal, _ := strconv.Atoi(string(digit))
            sum += pow(digitVal, p)
            p++
        }
        k := sum / n
        if sum == k*n {
            return k
        }
        return -1
    }
    
    func pow(base, exp int) int {
        result := 1
        for exp > 0 {
            if exp%2 != 0 {
                result *= base
            }
            base *= base
            exp /= 2
        }
        return result
    }
