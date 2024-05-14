Ordered count of Characters

    package orderedcount
    
    func OrderedCount(text string) []Tuple {
    	// Map to store the count of each character
    	countMap := make(map[rune]int)
    	// Slice to maintain the order of appearance
    	var order []rune
    
    	// Iterate through the text to count characters
    	for _, char := range text {
    		if _, found := countMap[char]; !found {
    			order = append(order, char)
    		}
    		countMap[char]++
    	}
    
    	// Create the result slice of Tuples
    	result := make([]Tuple, 0, len(order))
    	for _, char := range order {
    		result = append(result, Tuple{Char: char, Count: countMap[char]})
    	}
    
    	return result
    }
