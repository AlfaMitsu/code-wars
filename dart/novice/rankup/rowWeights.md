Row Weights

    List<int> rowWeights(List<int> weights) {
      var team1 = 0;
      var team2 = 0;
      
      for (var i = 0; i < weights.length; i++) {
        if (i % 2 == 0) {
          team1 += weights[i];
        } else {
          team2 += weights[i];
        }
      }
      
      return [team1, team2];
    }
