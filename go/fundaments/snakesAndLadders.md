Snakes and Ladders

    package kata
    
    import "fmt"
    
    // SnakesLadders - Structure that game is played on
    type SnakesLadders struct {
    	players   []int
    	positions map[int]int
    	turn      int
    	winner    int
    }
    
    // NewGame - Method that starts a new game for the SnakesLadders struct
    func (sl *SnakesLadders) NewGame() {
    	sl.players = []int{0, 0}
    	sl.positions = map[int]int{
    		2:  38, 7:  14, 8:  31, 15: 26, 16: 6, 21: 42,
    		28: 84, 36: 44, 46: 25, 49: 11, 51: 67, 62: 19,
    		64: 60, 71: 91, 74: 53, 78: 98, 87: 94, 89: 68,
    		92: 88, 95: 75, 99: 80,
    	}
    	sl.turn = 0
    	sl.winner = -1
    }
    
    // Play - Method that makes turn given a dice roll from die1 and die2 for the SnakesLadders struct
    // Player that dice is for should automatically be determined based on rules
    func (sl *SnakesLadders) Play(die1, die2 int) string {
    	if sl.winner != -1 {
    		return "Game over!"
    	}
    
    	player := sl.turn % 2
    	currentPosition := sl.players[player]
    	newPosition := currentPosition + die1 + die2
    
    	if newPosition > 100 {
    		newPosition = 200 - newPosition
    	}
    
    	// Check for ladder or snake
    	if val, ok := sl.positions[newPosition]; ok {
    		newPosition = val
    	}
    
    	sl.players[player] = newPosition
    
    	if newPosition == 100 {
    		sl.winner = player + 1
    		return fmt.Sprintf("Player %d Wins!", sl.winner)
    	}
    
    	if die1 != die2 {
    		sl.turn++
    	}
    
    	return fmt.Sprintf("Player %d is on square %d", player+1, newPosition)
    }
