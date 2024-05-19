Total amount of points

    package kata
    
    import "strings"
    
    func Points(games []string) int {
        points := 0
        for _, game := range games {
            scores := strings.Split(game, ":")
            x, y := scores[0], scores[1]
            if x > y {
                points += 3
            } else if x == y {
                points += 1
            }
        }
        return points
    }
