Recursion 101

    package kata
    
    func Solve(a, b int) []int {
    	for a != 0 && b != 0 {
    		if a >= 2*b {
    			a -= 2 * b
    		} else if b >= 2*a {
    			b -= 2 * a
    		} else {
    			break
    		}
    	}
    	return []int{a, b}
    }
