Positions Average

    package kata
    
    import "strings"
    
    func PosAverage(s string) float64 {
        substrings := strings.Split(s, ", ")
        n := len(substrings)
        totalPositions := n * (n - 1) / 2
        totalSamePositions := 0
    
        for i := 0; i < n; i++ {
            for j := i + 1; j < n; j++ {
                totalSamePositions += compareSubstrings(substrings[i], substrings[j])
            }
        }
    
        return float64(totalSamePositions) / float64(totalPositions * len(substrings[0])) * 100
    }
    
    func compareSubstrings(s1, s2 string) int {
        samePositions := 0
        for i := 0; i < len(s1); i++ {
            if s1[i] == s2[i] {
                samePositions++
            }
        }
        return samePositions
    }
