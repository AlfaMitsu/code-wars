Encrypt This!

    package kata
    
    import (
    	"strconv"
    	"strings"
    )
    
    func EncryptThis(text string) string {
    	words := strings.Split(text, " ")
    	result := ""
    	for _, word := range words {
    		if len(word) == 0 {
    			continue
    		}
    		firstChar := strconv.Itoa(int(word[0]))
    		if len(word) == 1 {
    			result += firstChar + " "
    			continue
    		}
    		if len(word) == 2 {
    			result += firstChar + string(word[1]) + " "
    			continue
    		}
    		result += firstChar + string(word[len(word)-1]) + word[2:len(word)-1] + string(word[1]) + " "
    	}
    	return strings.TrimSpace(result)
    }
