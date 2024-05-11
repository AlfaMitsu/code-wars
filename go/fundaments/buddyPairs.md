Buddy Pairs

    package kata
    
    func sumDivisors(n int) int {
        sum := 1 // Start with 1 since all numbers are divisible by 1
        for i := 2; i*i <= n; i++ {
            if n%i == 0 {
                sum += i
                if i*i != n {
                    sum += n / i
                }
            }
        }
        return sum
    }
    
    func Buddy(start, limit int) []int {
        for n := start; n <= limit; n++ {
            m := sumDivisors(n) - 1
            if m > n && sumDivisors(m) == n+1 {
                return []int{n, m}
            }
        }
        return nil
    }
