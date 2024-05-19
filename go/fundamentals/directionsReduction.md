Directions Reduction

    package kata
    
    func DirReduc(arr []string) []string {
        opposite := map[string]string{
            "NORTH": "SOUTH",
            "SOUTH": "NORTH",
            "EAST":  "WEST",
            "WEST":  "EAST",
        }
        
        result := []string{}
        
        for _, dir := range arr {
            if len(result) > 0 && result[len(result)-1] == opposite[dir] {
                result = result[:len(result)-1]
            } else {
                result = append(result, dir)
            }
        }
        
        return result
    }
