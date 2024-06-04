Duck Duck Goose
    
    function duckDuckGoose(players, goose) {
      const index = (goose - 1) % players.length;
      return players[index].name;
    }
