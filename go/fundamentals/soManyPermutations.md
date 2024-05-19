So many permutations

    package kata
    
    import "sort"
    
    func Permutations(s string) []string {
    	if len(s) <= 1 {
    		return []string{s}
    	}
    
    	var results []string
    	chars := []byte(s)
    	sort.Slice(chars, func(i, j int) bool { return chars[i] < chars[j] })
    	current := make([]byte, 0, len(chars))
    	visited := make([]bool, len(chars))
    	generatePermutations(chars, visited, current, &results)
    	return results
    }
    
    func generatePermutations(chars []byte, visited []bool, current []byte, results *[]string) {
    	if len(current) == len(chars) {
    		*results = append(*results, string(current))
    		return
    	}
    
    	for i, char := range chars {
    		if visited[i] || (i > 0 && !visited[i-1] && chars[i-1] == char) {
    			continue
    		}
    		visited[i] = true
    		current = append(current, char)
    		generatePermutations(chars, visited, current, results)
    		current = current[:len(current)-1]
    		visited[i] = false
    	}
    }
