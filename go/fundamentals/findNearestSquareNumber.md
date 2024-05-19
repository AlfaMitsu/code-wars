Find nearest square number

    package kata
    
    import "math"
    
    func NearestSq(n int) int {
        // Find the square root of n
        root := int(math.Sqrt(float64(n)))
    
        // Calculate the squares of root and root+1
        sq1 := root * root
        sq2 := (root + 1) * (root + 1)
    
        // Determine which square is closer to n
        if math.Abs(float64(n-sq1)) < math.Abs(float64(n-sq2)) {
            return sq1
        }
        return sq2
    }
