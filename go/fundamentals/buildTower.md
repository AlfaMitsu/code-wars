Build Tower

    package kata
    
    import (
        "strings"
    )
    
    func TowerBuilder(nFloors int) []string {
        var tower []string
        maxWidth := 2*nFloors - 1
        for i := 0; i < nFloors; i++ {
            stars := 2*i + 1
            spaces := (maxWidth - stars) / 2
            level := strings.Repeat(" ", spaces) + strings.Repeat("*", stars) + strings.Repeat(" ", spaces)
            tower = append(tower, level)
        }
        return tower
    }
