altERnaTIng cAsE <=> ALTerNAtiNG CaSe

    package kata
    
    import "unicode"
    
    func ToAlternatingCase(str string) string {
    	result := make([]rune, len(str))
    	for i, char := range str {
    		if unicode.IsLower(char) {
    			result[i] = unicode.ToUpper(char)
    		} else if unicode.IsUpper(char) {
    			result[i] = unicode.ToLower(char)
    		} else {
    			result[i] = char
    		}
    	}
    	return string(result)
    }
