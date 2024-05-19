Previous multiple of three

    package kata
    
    func PrevMultOfThree(n int) interface{} {
        for n > 0 {
            if n % 3 == 0 {
                return n
            }
            n /= 10
        }
        return nil
    }
