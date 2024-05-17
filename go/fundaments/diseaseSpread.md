Disease Spread

    package kata
    
    func Epidemic(tm, n, s0, i0 int, b, a float64) int {
        // Calculate dt
        dt := float64(tm) / float64(n)
    
        // Initialize the initial values
        S := float64(s0)
        I := float64(i0)
        R := 0.0
    
        // Variable to track the maximum number of infected individuals
        maxI := I
    
        // Iterate over each time step
        for k := 0; k < n; k++ {
            // Update the values using the finite difference formulas
            newS := S - dt * b * S * I
            newI := I + dt * (b * S * I - a * I)
            newR := R + dt * a * I
    
            // Update the current values
            S = newS
            I = newI
            R = newR
    
            // Update the maximum number of infected if the current value is greater
            if I > maxI {
                maxI = I
            }
        }
    
        // Return the maximum number of infected individuals as an integer
        return int(maxI)
    }
