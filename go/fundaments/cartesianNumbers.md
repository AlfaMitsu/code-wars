Cartesian Numbers

    package kata
    
    func CartesianNeighbor(x, y int) [][]int {
        neighbors := [][]int{}
        
        for dx := -1; dx <= 1; dx++ {
            for dy := -1; dy <= 1; dy++ {
                if dx == 0 && dy == 0 {
                    continue // Skip the current point
                }
                neighbors = append(neighbors, []int{x + dx, y + dy})
            }
        }
        
        return neighbors
    }
