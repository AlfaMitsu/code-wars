Reverse or Rotate?

    package kata
    
    import (
    	"strconv"
    )
    
    func Revrot(s string, n int) string {
    	if n <= 0 || s == "" || n > len(s) {
    		return ""
    	}
    
    	chunks := make([]string, 0)
    	for i := 0; i <= len(s)-n; i += n {
    		chunk := s[i : i+n]
    		sum := sumOfDigits(chunk)
    		if sum%2 == 0 {
    			chunks = append(chunks, reverse(chunk))
    		} else {
    			chunks = append(chunks, rotateLeft(chunk))
    		}
    	}
    
    	return concat(chunks)
    }
    
    func sumOfDigits(s string) int {
    	sum := 0
    	for _, c := range s {
    		digit, _ := strconv.Atoi(string(c))
    		sum += digit
    	}
    	return sum
    }
    
    func reverse(s string) string {
    	r := []rune(s)
    	for i, j := 0, len(r)-1; i < j; i, j = i+1, j-1 {
    		r[i], r[j] = r[j], r[i]
    	}
    	return string(r)
    }
    
    func rotateLeft(s string) string {
    	return s[1:] + string(s[0])
    }
    
    func concat(chunks []string) string {
    	result := ""
    	for _, chunk := range chunks {
    		result += chunk
    	}
    	return result
    }
