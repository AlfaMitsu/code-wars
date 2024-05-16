Getting along with Integer Partitions

    package kata
    
    import (
    	"fmt"
    	"math"
    	"sort"
    )
    
    // Part generates the partitions of a given integer n, calculates the product for each partition,
    // and returns the range, average, and median of these products.
    func Part(n int) string {
    	// Step 1: Generate all partitions of n
    	partitions := generatePartitions(n)
    
    	// Step 2: Calculate the product of each partition and store unique products
    	productSet := make(map[int]struct{})
    	for _, partition := range partitions {
    		product := 1
    		for _, num := range partition {
    			product *= num
    		}
    		productSet[product] = struct{}{}
    	}
    
    	// Convert productSet to a sorted slice
    	products := make([]int, 0, len(productSet))
    	for product := range productSet {
    		products = append(products, product)
    	}
    	sort.Ints(products)
    
    	// Step 3: Calculate range, average, and median
    	rangeVal := products[len(products)-1] - products[0]
    	averageVal := average(products)
    	medianVal := median(products)
    
    	// Step 4: Return the result as a formatted string
    	return fmt.Sprintf("Range: %d Average: %.2f Median: %.2f", rangeVal, averageVal, medianVal)
    }
    
    // generatePartitions generates all partitions of a given integer n.
    func generatePartitions(n int) [][]int {
    	var partitions [][]int
    	var partition []int
    	var generate func(int, int)
    	generate = func(n, max int) {
    		if n == 0 {
    			partCopy := make([]int, len(partition))
    			copy(partCopy, partition)
    			partitions = append(partitions, partCopy)
    			return
    		}
    		for i := int(math.Min(float64(max), float64(n))); i >= 1; i-- {
    			partition = append(partition, i)
    			generate(n-i, i)
    			partition = partition[:len(partition)-1]
    		}
    	}
    	generate(n, n)
    	return partitions
    }
    
    // average calculates the average of a slice of integers.
    func average(arr []int) float64 {
    	sum := 0
    	for _, num := range arr {
    		sum += num
    	}
    	return float64(sum) / float64(len(arr))
    }
    
    // median calculates the median of a slice of integers.
    func median(arr []int) float64 {
    	length := len(arr)
    	if length%2 == 0 {
    		return float64(arr[length/2-1]+arr[length/2]) / 2.0
    	}
    	return float64(arr[length/2])
    }
