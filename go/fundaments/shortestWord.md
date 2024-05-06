Shortest Word

    package kata
    
    import (
    	"strings"
    	"math"
    )
    
    func FindShort(s string) int {
    	words := strings.Split(s, " ")
    	shortest := math.MaxInt32
    	for _, word := range words {
    		wordLength := len(word)
    		if wordLength < shortest {
    			shortest = wordLength
    		}
    	}
    	return shortest
    }
