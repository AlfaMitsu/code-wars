EUFA EURO 2016
    
    function uefaEuro2016(teams, scores) {
      // Destructure the arrays to get the team names and their scores
      const [team1, team2] = teams;
      const [score1, score2] = scores;
      
      // Determine the result of the match
      if (score1 > score2) {
        return `At match ${team1} - ${team2}, ${team1} won!`;
      } else if (score1 < score2) {
        return `At match ${team1} - ${team2}, ${team2} won!`;
      } else {
        return `At match ${team1} - ${team2}, teams played draw.`;
      }
    }
    
    // Example usage:
    console.log(uefaEuro2016(['Germany', 'Ukraine'], [2, 0])); // "At match Germany - Ukraine, Germany won!"
    console.log(uefaEuro2016(['Belgium', 'Italy'], [0, 2])); // "At match Belgium - Italy, Italy won!"
    console.log(uefaEuro2016(['Portugal', 'Iceland'], [1, 1])); // "At match Portugal - Iceland, teams played draw."
