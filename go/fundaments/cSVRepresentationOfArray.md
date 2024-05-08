CSV representation of array

    package kata
    
    import (
        "bytes"
        "strconv"
    )
    
    func ToCsvText(array [][]int) string {
        var result bytes.Buffer
    
        for i, row := range array {
            for j, num := range row {
                result.WriteString(strconv.Itoa(num))
                if j != len(row)-1 {
                    result.WriteRune(',')
                }
            }
            if i != len(array)-1 {
                result.WriteRune('\n')
            }
        }
    
        return result.String()
    }
