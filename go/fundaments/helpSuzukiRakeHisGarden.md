Help Suzuki rake his garden

    package kata
    
    import "strings"
    
    func RakeGarden(garden string) string {
        // Split the garden string into individual words
        words := strings.Split(garden, " ")
    
        // Replace non-rock and non-gravel items with "gravel"
        for i, word := range words {
            if word != "rock" && word != "gravel" {
                words[i] = "gravel"
            }
        }
    
        // Join the words back into a string
        result := strings.Join(words, " ")
    
        return result
    }
