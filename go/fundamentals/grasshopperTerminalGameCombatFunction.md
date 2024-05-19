Grasshopper - Terminal game combat function

    package kata
    
    func combat(health, damage float64) float64 {
        newHealth := health - damage
        if newHealth < 0 {
            return 0
        }
        return newHealth
    }
