Sort and Star

    package kata
    
    import (
        "sort"
        "strings"
    )
    
    func TwoSort(arr []string) string {
        sort.Strings(arr)
        firstWord := arr[0]
        return strings.Join(strings.Split(firstWord, ""), "***")
    }
