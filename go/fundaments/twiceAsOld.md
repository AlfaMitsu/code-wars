Twice as Old

    package kata
    
    func TwiceAsOld(dadYearsOld, sonYearsOld int) int {
        years := dadYearsOld - 2*sonYearsOld
        if years < 0 {
            years = -years
        }
        return years
    }
