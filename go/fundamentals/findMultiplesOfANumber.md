Find multiples of a number

    package kata
    
    func FindMultiples(integer, limit int) []int {
    	multiples := []int{}
    	for i := 1; integer*i <= limit; i++ {
    		multiples = append(multiples, integer*i)
    	}
    	return multiples
    }
