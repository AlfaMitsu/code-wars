Going to the Cinema

    package kata
    
    import (
    	"math"
    )
    
    func Movie(card, ticket int, perc float64) int {
    	count := 0
    	priceA := 0
    	priceB := float64(card)
    
    	for {
    		count++
    		priceA += ticket
    		priceB += float64(ticket) * math.Pow(perc, float64(count))
    		if math.Ceil(priceB) < float64(priceA) {
    			break
    		}
    	}
    
    	return count
    }
