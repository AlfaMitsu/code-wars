Reducing by Steps

    package kata
    
    // Gcdi calculates the greatest common divisor of x and y
    func Gcdi(x, y int) int {
        if x < 0 {
            x = -x
        }
        if y < 0 {
            y = -y
        }
        for y != 0 {
            x, y = y, x%y
        }
        return x
    }
    
    // Som returns the sum of x and y
    func Som(x, y int) int {
        return x + y
    }
    
    // Maxi returns the maximum of x and y
    func Maxi(x, y int) int {
        if x > y {
            return x
        }
        return y
    }
    
    // Mini returns the minimum of x and y
    func Mini(x, y int) int {
        if x < y {
            return x
        }
        return y
    }
    
    // Lcmu calculates the least common multiple of x and y
    func Lcmu(x, y int) int {
        if x < 0 {
            x = -x
        }
        if y < 0 {
            y = -y
        }
        return x * (y / Gcdi(x, y))
    }
    
    type FParam func(int, int) int
    
    // OperArray applies the function f iteratively to the array starting with init value
    func OperArray(f FParam, arr []int, init int) []int {
        result := make([]int, len(arr))
        current := init
        for i, v := range arr {
            current = f(current, v)
            result[i] = current
        }
        return result
    }
