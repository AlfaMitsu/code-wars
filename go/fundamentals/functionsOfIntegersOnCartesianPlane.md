Functions of Integers on Cartesian Plane

    package kata
    
    func SuMin(m int) int64 {
        n := int64(m)
        sum := int64(0)
        for y := int64(1); y <= n; y++ {
            sum += y * (n - y) + y * (y + 1) / 2
        }
        return sum
    }
    
    func SuMax(m int) int64 {
        n := int64(m)
        sum := int64(0)
        for y := int64(1); y <= n; y++ {
            sum += y * y + (n * (n + 1) / 2) - (y * (y + 1) / 2)
        }
        return sum
    }
    
    func SumSum(m int) int64 {
        n := int64(m)
        sum := n * n * (n + 1)
        return sum
    }
