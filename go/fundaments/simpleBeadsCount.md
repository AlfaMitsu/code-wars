Simple Beads Count

    package kata
    
    func CountRedBeads(n int) int {
        if n < 2 {
            return 0
        }
        return 2 * (n - 1)
    }
