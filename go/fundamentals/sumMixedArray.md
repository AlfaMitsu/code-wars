Sum Mixed Array

    package kata
    
    import (
        "strconv"
    )
    
    func SumMix(arr []interface{}) int {
        sum := 0
        for _, v := range arr {
            switch val := v.(type) {
            case int:
                sum += val
            case string:
                num, _ := strconv.Atoi(val)
                sum += num
            }
        }
        return sum
    }
