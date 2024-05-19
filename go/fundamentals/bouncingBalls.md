Bouncing Balls

    package kata
    
    func BouncingBall(h, bounce, window float64) int {
        if h <= 0 || bounce <= 0 || bounce >= 1 || window >= h {
            return -1
        }
    
        count := 0
        for h > window {
            // Falling past the window
            count++
            h *= bounce
            // Bouncing back past the window
            if h > window {
                count++
            }
        }
    
        return count
    }
