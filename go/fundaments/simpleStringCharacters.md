Simple String Characters

    package kata
    
    import (
    	"unicode"
    )
    
    func Solve(s string) []int {
    	uppercaseCount := 0
    	lowercaseCount := 0
    	numberCount := 0
    	specialCount := 0
    
    	for _, char := range s {
    		if unicode.IsUpper(char) {
    			uppercaseCount++
    		} else if unicode.IsLower(char) {
    			lowercaseCount++
    		} else if unicode.IsDigit(char) {
    			numberCount++
    		} else {
    			specialCount++
    		}
    	}
    
    	return []int{uppercaseCount, lowercaseCount, numberCount, specialCount}
    }
