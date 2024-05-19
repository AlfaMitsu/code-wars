PI Approximation

    package kata
    
    import (
        "math"
        "fmt"
    )
    
    func IterPi(epsilon float64) (int, string) {
        pi := 0.0
        iteration := 0
        sign := 1.0
        
        for math.Abs(math.Pi-pi*4) >= epsilon {
            pi += sign / (float64(iteration)*2 + 1)
            sign = -sign
            iteration++
        }
        
        return iteration, fmt.Sprintf("%.10f", pi*4)
    }
