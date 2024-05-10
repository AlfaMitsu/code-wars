Scaling Squared Strings

    package kata
    
    import (
    	"strings"
    )
    
    func Scale(s string, k, n int) string {
    	if s == "" {
    		return ""
    	}
    
    	lines := strings.Split(s, "\n")
    	var result strings.Builder
    
    	for i, line := range lines {
    		for v := 0; v < n; v++ {
    			for _, char := range line {
    				for h := 0; h < k; h++ {
    					result.WriteRune(char)
    				}
    			}
    			if i < len(lines)-1 || v < n-1 {
    				result.WriteRune('\n')
    			}
    		}
    	}
    
    	return result.String()
    }
