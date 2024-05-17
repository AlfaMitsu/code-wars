Parabolic Arc Length

    package kata
    
    import "math"
    
    // Function to approximate the length of the curve y = x^2 from 0 to 1 with n sub-intervals
    func LenCurve(n int) float64 {
        if n <= 0 {
            return 0
        }
        
        h := 1.0 / float64(n)
        length := 0.0
    
        for i := 0; i < n; i++ {
            x0 := float64(i) * h
            y0 := x0 * x0
            x1 := float64(i+1) * h
            y1 := x1 * x1
    
            // Calculate the distance between (x0, y0) and (x1, y1)
            dx := x1 - x0
            dy := y1 - y0
            segmentLength := math.Sqrt(dx*dx + dy*dy)
            
            length += segmentLength
        }
        
        return length
    }
