Digital Cypher

    package kata
    
    import (
        "strconv"
    )
    
    func Encode(str string, key int) []int {
        keyStr := strconv.Itoa(key)
        keyLen := len(keyStr)
        keyIndex := 0
        
        result := make([]int, len(str))
        for i, char := range str {
            charNum := int(char - 'a' + 1)
            keyDigit, _ := strconv.Atoi(string(keyStr[keyIndex]))
            result[i] = charNum + keyDigit
            keyIndex++
            if keyIndex >= keyLen {
                keyIndex = 0
            }
        }
        
        return result
    }
