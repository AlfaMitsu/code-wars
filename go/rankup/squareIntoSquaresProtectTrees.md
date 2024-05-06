Square into Squares. Protect trees!

    package kata
    
    func Decompose(n int64) []int64 {
    	// Define a recursive function to find the sequence of numbers whose squares sum up to n^2
    	var decomposeHelper func(remaining, current int64) []int64
    	decomposeHelper = func(remaining, current int64) []int64 {
    		if remaining == 0 {
    			return []int64{}
    		}
    		for i := current - 1; i > 0; i-- {
    			if i*i <= remaining {
    				if result := decomposeHelper(remaining-i*i, i); result != nil {
    					return append(result, i)
    				}
    			}
    		}
    		return nil
    	}
    
    	result := decomposeHelper(n*n, n)
    	if result != nil {
    		return result
    	}
    	return nil
    }
