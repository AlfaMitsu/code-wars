Diophantine Equation

    package kata
    
    import (
    	"math"
    )
    
    func Solequa(n int) [][]int {
    	result := [][]int{}
    
    	for i := 1; i <= int(math.Sqrt(float64(n))); i++ {
    		if n%i == 0 {
    			j := n / i
    			if (i+j)%2 == 0 && (j-i)%4 == 0 {
    				x := (i + j) / 2
    				y := (j - i) / 4
    				result = append(result, []int{x, y})
    			}
    		}
    	}
    
    	return result
    }
