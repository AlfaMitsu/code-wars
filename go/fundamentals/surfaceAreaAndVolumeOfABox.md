Surface Area and Volume of a Box

    package kata
    
    func GetSize(w, h, d int) [2]int {
        area := 2*(w*h + h*d + w*d)
        volume := w * h * d
        return [2]int{area, volume}
    }
