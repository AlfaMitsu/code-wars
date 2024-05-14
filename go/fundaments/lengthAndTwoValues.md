Length and Two Values

    package kata
    
    func Alternate(n int, firstValue string, secondValue string) []string {
    	result := make([]string, n)
    	for i := 0; i < n; i++ {
    		if i%2 == 0 {
    			result[i] = firstValue
    		} else {
    			result[i] = secondValue
    		}
    	}
    	return result
    }
