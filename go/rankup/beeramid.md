Beeramid

    package kata
    
    func Beeramid(bonus int, price float64) int {
        cans := float64(bonus) / price
        level := 0
        for cans >= float64(level+1)*float64(level+1) {
            level++
            cans -= float64(level * level)
        }
        return level
    }
