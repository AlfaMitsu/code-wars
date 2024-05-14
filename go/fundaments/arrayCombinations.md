Array Combinations

    package kata
    
    import "fmt"
    
    func Solve(data [][]int) int {
    	uniqueArrays := make(map[string]bool)
    	generateUniqueArrays(data, []int{}, uniqueArrays)
    	return len(uniqueArrays)
    }
    
    func generateUniqueArrays(data [][]int, current []int, uniqueArrays map[string]bool) {
    	if len(current) == len(data) {
    		key := getKey(current)
    		uniqueArrays[key] = true
    		return
    	}
    
    	for _, num := range data[len(current)] {
    		newCurrent := append(current, num)
    		generateUniqueArrays(data, newCurrent, uniqueArrays)
    	}
    }
    
    func getKey(nums []int) string {
    	key := ""
    	for _, num := range nums {
    		key += "|" + fmt.Sprint(num)
    	}
    	return key
    }
