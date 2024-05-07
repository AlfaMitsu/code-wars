Functional Addition

    package kata
    
    func Add(n int) func(int) int {
        return func(x int) int {
            return x + n
        }
    }
