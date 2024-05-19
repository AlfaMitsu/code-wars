Multiplication table for Number

    package kata
    
    import "fmt"
    
    func MultiTable(number int) string {
        table := ""
        for i := 1; i <= 10; i++ {
            if i > 1 {
                table += "\n"
            }
            table += fmt.Sprintf("%d * %d = %d", i, number, i*number)
        }
        return table
    }
