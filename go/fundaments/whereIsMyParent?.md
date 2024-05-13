Where is my parent?

    package kata
    
    import (
        "sort"
        "strings"
        "unicode"
    )
    
    func FindChildren(dancingBrigade string) string {
        // Split the input string into a slice of characters
        chars := strings.Split(dancingBrigade, "")
    
        // Sort the characters alphabetically
        sort.Strings(chars)
    
        // Join the sorted characters back into a string
        sortedString := strings.Join(chars, "")
    
        // Create a map to store the children of each mother
        childrenMap := make(map[string]string)
    
        // Iterate over the sorted string to group mothers and their children
        for _, char := range sortedString {
            if unicode.IsUpper(char) {
                childrenMap[string(char)] = ""
            } else {
                mother := strings.ToUpper(string(char))
                childrenMap[mother] += string(char)
            }
        }
    
        // Build the final sorted string with mothers followed by their children
        var result strings.Builder
        for _, char := range sortedString {
            if unicode.IsUpper(char) {
                result.WriteString(string(char))
                result.WriteString(childrenMap[string(char)])
            }
        }
    
        return result.String()
    }
