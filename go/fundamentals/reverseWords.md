Reverse Words

    package kata
    
    import (
    	"strings"
    )
    
    func ReverseWords(str string) string {
    	var result strings.Builder
    	var word strings.Builder
    	for _, char := range str {
    		if char == ' ' {
    			if word.Len() > 0 {
    				result.WriteString(reverseString(word.String()))
    				word.Reset()
    			}
    			result.WriteRune(char)
    		} else {
    			word.WriteRune(char)
    		}
    	}
    	if word.Len() > 0 {
    		result.WriteString(reverseString(word.String()))
    	}
    	return result.String()
    }
    
    func reverseString(s string) string {
    	runes := []rune(s)
    	for i, j := 0, len(runes)-1; i < j; i, j = i+1, j-1 {
    		runes[i], runes[j] = runes[j], runes[i]
    	}
    	return string(runes)
    }
