Fibonacci

    package kata
    
    func Fib(n int) int {
        if n < 0 {
            return -1 // assuming negative input is invalid for Fibonacci sequence
        }
        if n == 0 {
            return 0
        }
        if n == 1 {
            return 1
        }
    
        a, b := 0, 1
        for i := 2; i <= n; i++ {
            a, b = b, a+b
        }
        return b
    }
