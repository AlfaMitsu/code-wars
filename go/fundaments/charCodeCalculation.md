Char Code Calculation

    package kata
    
    import (
        "strconv"
        "strings"
    )
    
    func Calc(s string) int {
        // Convert each character to its ASCII code
        var total1 string
        for _, char := range s {
            total1 += strconv.Itoa(int(char))
        }
    
        // Replace '7' with '1' in total1
        total2 := strings.ReplaceAll(total1, "7", "1")
    
        // Calculate the sum of digits in total1 and total2
        sum1 := sumDigits(total1)
        sum2 := sumDigits(total2)
    
        // Return the difference
        return sum1 - sum2
    }
    
    func sumDigits(s string) int {
        sum := 0
        for _, char := range s {
            digit, _ := strconv.Atoi(string(char))
            sum += digit
        }
        return sum
    }
