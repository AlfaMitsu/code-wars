Most Valuable Character

    package kata
    
    func Solve(s string) rune {
    	firstOccurrence := make(map[rune]int)
    	lastOccurrence := make(map[rune]int)
    
    	for i, ch := range s {
    		if _, exists := firstOccurrence[ch]; !exists {
    			firstOccurrence[ch] = i
    		}
    		lastOccurrence[ch] = i
    	}
    
    	var maxChar rune
    	maxValue := -1
    
    	for ch, firstIdx := range firstOccurrence {
    		lastIdx := lastOccurrence[ch]
    		value := lastIdx - firstIdx
    
    		if value > maxValue || (value == maxValue && ch < maxChar) {
    			maxValue = value
    			maxChar = ch
    		}
    	}
    
    	return maxChar
    }
