Count of positives / sum of negatives

    package kata
    
    func CountPositivesSumNegatives(numbers []int) []int {
        if len(numbers) == 0 {
            return []int{}
        }
    
        countPositives := 0
        sumNegatives := 0
    
        for _, num := range numbers {
            if num > 0 {
                countPositives++
            } else {
                sumNegatives += num
            }
        }
    
        return []int{countPositives, sumNegatives}
    }
