Snail

    package kata
    
    func Snail(snailMap [][]int) []int {
    	if len(snailMap) == 0 || len(snailMap[0]) == 0 {
    		return []int{}
    	}
    
    	var result []int
    	rowBegin, rowEnd := 0, len(snailMap)-1
    	colBegin, colEnd := 0, len(snailMap[0])-1
    
    	for rowBegin <= rowEnd && colBegin <= colEnd {
    		// Move right
    		for i := colBegin; i <= colEnd; i++ {
    			result = append(result, snailMap[rowBegin][i])
    		}
    		rowBegin++
    
    		// Move down
    		for i := rowBegin; i <= rowEnd; i++ {
    			result = append(result, snailMap[i][colEnd])
    		}
    		colEnd--
    
    		// Move left
    		if rowBegin <= rowEnd {
    			for i := colEnd; i >= colBegin; i-- {
    				result = append(result, snailMap[rowEnd][i])
    			}
    			rowEnd--
    		}
    
    		// Move up
    		if colBegin <= colEnd {
    			for i := rowEnd; i >= rowBegin; i-- {
    				result = append(result, snailMap[i][colBegin])
    			}
    			colBegin++
    		}
    	}
    
    	return result
    }
