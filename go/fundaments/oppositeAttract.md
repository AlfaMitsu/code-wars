Opposite Attract

    package kata
    
    import "fmt"
    
    func LoveFunc(flower1, flower2 int) bool {
        return (flower1%2 == 0 && flower2%2 != 0) || (flower1%2 != 0 && flower2%2 == 0)
    }
    
    func main() {
        flower1 := 3
        flower2 := 4
        fmt.Println(LoveFunc(flower1, flower2)) // Output: true
    }
