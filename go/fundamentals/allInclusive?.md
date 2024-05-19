All Inclusive?

    package kata
    
    func ContainAllRots(strng string, arr []string) bool {
        if strng == "" {
            return true
        }
    
        for i := 0; i < len(strng); i++ {
            rot := strng[i:] + strng[:i]
            found := false
            for _, s := range arr {
                if s == rot {
                    found = true
                    break
                }
            }
            if !found {
                return false
            }
        }
    
        return true
    }
