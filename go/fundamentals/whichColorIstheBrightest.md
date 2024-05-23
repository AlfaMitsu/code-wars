Which color is the brightest?

    package kata
    
    import (
        "strconv"
    )
    
    func Brightest(colors []string) string {
        brightest := ""
        maxBrightness := -1
    
        for _, color := range colors {
            brightness := getBrightness(color)
            if brightness > maxBrightness {
                maxBrightness = brightness
                brightest = color
            }
        }
    
        return brightest
    }
    
    func getBrightness(color string) int {
        r, _ := strconv.ParseInt(color[1:3], 16, 32)
        g, _ := strconv.ParseInt(color[3:5], 16, 32)
        b, _ := strconv.ParseInt(color[5:7], 16, 32)
    
        return int(max(int(r), max(int(g), int(b))))
    }
    
    func max(a, b int) int {
        if a > b {
            return a
        }
        return b
    }
