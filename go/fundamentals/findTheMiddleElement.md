Find the Middle Element

    package kata
    
    func Gimme(array [3]int) int {
        minIndex, maxIndex := 0, 0
        for i := range array {
            if array[i] < array[minIndex] {
                minIndex = i
            }
            if array[i] > array[maxIndex] {
                maxIndex = i
            }
        }
    
        for i := range array {
            if i != minIndex && i != maxIndex {
                return i
            }
        }
    
        return -1 // Error: No middle element found
    }
