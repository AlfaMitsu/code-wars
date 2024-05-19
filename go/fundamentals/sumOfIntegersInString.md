Sum of integers in string

    package kata
    
    import (
    	"regexp"
    	"strconv"
    )
    
    // SumOfIntegersInString calculates the sum of the integers inside a string
    func SumOfIntegersInString(strng string) int {
    	// Regular expression to find all integers in the string
    	re := regexp.MustCompile(`\d+`)
    
    	// Find all substrings that match the regular expression (integers)
    	matches := re.FindAllString(strng, -1)
    
    	sum := 0
    	// Convert each matched substring to an integer and sum them up
    	for _, match := range matches {
    		num, _ := strconv.Atoi(match)
    		sum += num
    	}
    
    	return sum
    }
