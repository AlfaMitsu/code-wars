Highest and Lowest

    package kata
    
    import (
    	"fmt"
    	"strconv"
    	"strings"
    )
    
    func HighAndLow(in string) string {
    	// Split the input string into individual numbers
    	nums := strings.Split(in, " ")
    
    	// Initialize variables to store the highest and lowest numbers
    	highest, _ := strconv.Atoi(nums[0])
    	lowest, _ := strconv.Atoi(nums[0])
    
    	// Iterate through the numbers and update the highest and lowest values
    	for _, numStr := range nums[1:] {
    		num, _ := strconv.Atoi(numStr)
    		if num > highest {
    			highest = num
    		}
    		if num < lowest {
    			lowest = num
    		}
    	}
    
    	// Return the highest and lowest numbers as a string
    	return fmt.Sprintf("%d %d", highest, lowest)
    }
