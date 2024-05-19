Help your Granny

    package kata
    
    import (
        "math"
    )
    
    func Tour(arrFriends []string, ftwns map[string]string, h map[string]float64) int {
        totalDistance := 0.0
        var prevTown string
    
        for _, friend := range arrFriends {
            town, ok := ftwns[friend]
            if !ok {
                continue
            }
    
            distance, ok := h[town]
            if !ok {
                continue
            }
    
            if prevTown != "" {
                prevDistance, _ := h[prevTown]
                totalDistance += math.Sqrt(math.Pow(distance, 2) - math.Pow(prevDistance, 2))
            } else {
                totalDistance += distance
            }
    
            prevTown = town
        }
    
        if prevTown != "" {
            prevDistance, _ := h[prevTown]
            totalDistance += prevDistance
        }
    
        return int(totalDistance)
    }
