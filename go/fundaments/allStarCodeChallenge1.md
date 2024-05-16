All Star Code Challenge #1

    package kata
    
    // NBAPlayer struct represents a basketball player with a team and points per game (PPG)
    type NBAPlayer struct {
      Team string
      Ppg  float64
    }
    
    // SumPpg function takes two NBAPlayer structs and returns the sum of their Ppg fields
    func SumPpg(playerOne, playerTwo NBAPlayer) float64 {
      return playerOne.Ppg + playerTwo.Ppg
    }
