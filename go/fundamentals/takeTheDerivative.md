Take the Derivative

    package kata
    
    import "fmt"
    
    func Derive(coefficient, exponent int) string {
        product := coefficient * exponent
        newExponent := exponent - 1
        if newExponent == 1 {
            return fmt.Sprintf("%dx", product)
        }
        return fmt.Sprintf("%dx^%d", product, newExponent)
    }
