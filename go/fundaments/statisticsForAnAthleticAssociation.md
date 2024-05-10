Statistics for an Athletic Association

    package kata
    
    import (
        "sort"
        "strings"
        "strconv"
    )
    
    func Stati(strg string) string {
        if strg == "" {
            return ""
        }
    
        times := strings.Split(strg, ", ")
        totalSeconds := make([]int, len(times))
        for i, t := range times {
            parts := strings.Split(t, "|")
            h, _ := strconv.Atoi(parts[0])
            m, _ := strconv.Atoi(parts[1])
            s, _ := strconv.Atoi(parts[2])
            totalSeconds[i] = h*3600 + m*60 + s
        }
    
        sort.Ints(totalSeconds)
    
        rangeSeconds := totalSeconds[len(totalSeconds)-1] - totalSeconds[0]
        averageSeconds := sum(totalSeconds) / len(totalSeconds)
        medianSeconds := median(totalSeconds)
    
        return "Range: " + formatTime(rangeSeconds) +
            " Average: " + formatTime(averageSeconds) +
            " Median: " + formatTime(medianSeconds)
    }
    
    func sum(arr []int) int {
        sum := 0
        for _, v := range arr {
            sum += v
        }
        return sum
    }
    
    func median(arr []int) int {
        mid := len(arr) / 2
        if len(arr)%2 == 0 {
            return (arr[mid-1] + arr[mid]) / 2
        }
        return arr[mid]
    }
    
    func formatTime(seconds int) string {
        h := seconds / 3600
        m := (seconds % 3600) / 60
        s := seconds % 60
        return pad(h) + "|" + pad(m) + "|" + pad(s)
    }
    
    func pad(num int) string {
        return strconv.Itoa(num/10) + strconv.Itoa(num%10)
    }
