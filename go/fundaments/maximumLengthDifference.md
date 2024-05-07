Maximum Length Difference

    package kata
    
    import (
        "math"
    )
    
    func MxDifLg(a1 []string, a2 []string) int {
        if len(a1) == 0 || len(a2) == 0 {
            return -1
        }
    
        max1, min1 := findMaxLengthAndMinLength(a1)
        max2, min2 := findMaxLengthAndMinLength(a2)
    
        return int(math.Max(math.Abs(float64(max1 - min2)), math.Abs(float64(max2 - min1))))
    }
    
    func findMaxLengthAndMinLength(arr []string) (int, int) {
        maxLength := len(arr[0])
        minLength := len(arr[0])
    
        for _, s := range arr {
            if len(s) > maxLength {
                maxLength = len(s)
            }
            if len(s) < minLength {
                minLength = len(s)
            }
        }
    
        return maxLength, minLength
    }
