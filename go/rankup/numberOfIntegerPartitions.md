Number of Integer Partitions

    package kata
    
    func Partitions(n int) int {
    	// Create a 2D slice to store the partition counts
    	// dp[i][j] will store the number of partitions of i using integers up to j
    	dp := make([][]int, n+1)
    	for i := range dp {
    		dp[i] = make([]int, n+1)
    	}
    
    	// Initialize base cases
    	for i := 0; i <= n; i++ {
    		dp[0][i] = 1 // Only one way to partition 0
    	}
    
    	// Calculate the number of partitions using dynamic programming
    	for i := 1; i <= n; i++ {
    		for j := 1; j <= n; j++ {
    			if j <= i {
    				dp[i][j] = dp[i][j-1] + dp[i-j][j]
    			} else {
    				dp[i][j] = dp[i][j-1]
    			}
    		}
    	}
    
    	return dp[n][n]
    }
