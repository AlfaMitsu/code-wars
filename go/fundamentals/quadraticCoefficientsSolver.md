Quadratic Coefficients Solver

    package kata
    
    func Quadratic(x1, x2 int) [3]int {
        // Since a is fixed to 1, the coefficient of x^2 is 1
        // For a quadratic equation (x - x1) * (x - x2) = 0
        // The expanded form is x^2 - (x1 + x2)x + x1*x2 = 0
        // So, b = -(x1 + x2) and c = x1*x2
        b := -(x1 + x2)
        c := x1 * x2
        return [3]int{1, b, c}
    }
