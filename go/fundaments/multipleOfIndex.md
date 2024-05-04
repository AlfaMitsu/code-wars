Multiple of Index

    package kata
    
    func multipleOfIndex(ints []int) []int {
        result := []int{}
        for i, num := range ints {
            if i != 0 && num%i == 0 {
                result = append(result, num)
            }
        }
        return result
    }
