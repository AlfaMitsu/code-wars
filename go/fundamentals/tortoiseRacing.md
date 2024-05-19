Tortoise Racing

    package kata
    
    func Race(v1, v2, g int) [3]int {
        // If v2 is not greater than v1, return -1, -1, -1 as specified.
        if v1 >= v2 {
            return [3]int{-1, -1, -1}
        }
    
        // Calculate the relative speed (v2 - v1)
        relativeSpeed := v2 - v1
        
        // Calculate the time it takes for B to catch A in seconds
        timeInSeconds := g * 3600 / relativeSpeed
        
        // Convert the time to hours, minutes, and seconds
        hours := timeInSeconds / 3600
        minutes := (timeInSeconds % 3600) / 60
        seconds := timeInSeconds % 60
        
        // Return the result as an array [hours, minutes, seconds]
        return [3]int{hours, minutes, seconds}
    }
