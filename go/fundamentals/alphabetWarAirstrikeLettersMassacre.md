Alphabet war - airstrike - letters massacre

    package kata
    
    func AlphabetWar(fight string) string {
    	leftPower := map[rune]int{'w': 4, 'p': 3, 'b': 2, 's': 1}
    	rightPower := map[rune]int{'m': 4, 'q': 3, 'd': 2, 'z': 1}
    
    	// Step 1: Handle the bombs
    	processedFight := []rune(fight)
    	for i := 0; i < len(processedFight); i++ {
    		if processedFight[i] == '*' {
    			if i > 0 && processedFight[i-1] != '*' {
    				processedFight[i-1] = '_'
    			}
    			if i < len(processedFight)-1 && processedFight[i+1] != '*' {
    				processedFight[i+1] = '_'
    			}
    			processedFight[i] = '_'
    		}
    	}
    
    	// Step 2: Calculate the scores
    	leftScore := 0
    	rightScore := 0
    	for _, char := range processedFight {
    		if score, found := leftPower[char]; found {
    			leftScore += score
    		} else if score, found := rightPower[char]; found {
    			rightScore += score
    		}
    	}
    
    	// Step 3: Determine the winner
    	if leftScore > rightScore {
    		return "Left side wins!"
    	} else if rightScore > leftScore {
    		return "Right side wins!"
    	} else {
    		return "Let's fight again!"
    	}
    }
