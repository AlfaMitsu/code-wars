Rotate for a max

    package kata
    
    import (
        "strconv"
    )
    
    func MaxRot(n int64) int64 {
        str := strconv.FormatInt(n, 10)
        max := n
        for i := 0; i < len(str)-1; i++ {
            str = str[:i] + str[i+1:] + str[i:i+1]
            num, _ := strconv.ParseInt(str, 10, 64)
            if num > max {
                max = num
            }
        }
        return max
    }
