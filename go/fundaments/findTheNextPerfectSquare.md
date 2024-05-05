Find the next perfect square!

    package kata
    
    import "math"
    
    func FindNextSquare(sq int64) int64 {
        root := int64(math.Sqrt(float64(sq)))
        if root*root == sq {
            return (root + 1) * (root + 1)
        }
        return -1
    }
