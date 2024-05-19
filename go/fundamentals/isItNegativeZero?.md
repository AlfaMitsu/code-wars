Is It Negative Zero (-0)?

    package kata
    
    import "math"
    
    func IsNegativeZero(n float64) bool {
        return n == 0 && math.Signbit(n)
    }
