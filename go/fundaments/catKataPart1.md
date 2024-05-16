Cat Kata Part 1

    package kata
    
    import (
    	"math"
    )
    
    func PeacefulYard(yard []string, minDistance int) bool {
    	type Position struct {
    		x, y int
    	}
    	var cats []Position
    
    	// Find the positions of all the cats
    	for i := 0; i < len(yard); i++ {
    		for j := 0; j < len(yard[i]); j++ {
    			if yard[i][j] == 'L' || yard[i][j] == 'M' || yard[i][j] == 'R' {
    				cats = append(cats, Position{x: i, y: j})
    			}
    		}
    	}
    
    	// If there are one or no cats, return true
    	if len(cats) <= 1 {
    		return true
    	}
    
    	// Function to calculate Euclidean distance
    	distance := func(p1, p2 Position) float64 {
    		return math.Sqrt(float64((p1.x-p2.x)*(p1.x-p2.x) + (p1.y-p2.y)*(p1.y-p2.y)))
    	}
    
    	// Check distances between every pair of cats
    	for i := 0; i < len(cats)-1; i++ {
    		for j := i + 1; j < len(cats); j++ {
    			if distance(cats[i], cats[j]) < float64(minDistance) {
    				return false
    			}
    		}
    	}
    
    	return true
    }
