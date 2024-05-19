Number of Decimal Digits

    package kata
    
    import "strconv"
    
    func Digits(n uint64) int {
        return len(strconv.FormatUint(n, 10))
    }
