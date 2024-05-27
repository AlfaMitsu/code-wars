Number of people in the bus

    var number = function(busStops) {
      // Initialize the number of people on the bus to 0
      let peopleOnBus = 0;
      
      // Iterate over each bus stop
      for (let i = 0; i < busStops.length; i++) {
        // Add the number of people getting on the bus
        peopleOnBus += busStops[i][0];
        // Subtract the number of people getting off the bus
        peopleOnBus -= busStops[i][1];
      }
      
      // Return the number of people remaining on the bus
      return peopleOnBus;
    }
    
    // Example usage:
    console.log(number([[10, 0], [3, 5], [5, 8]])); // 5
    console.log(number([[3, 0], [9, 1], [4, 10], [12, 2], [6, 1], [7, 10]])); // 17
    console.log(number([[3, 0], [9, 1], [4, 8], [12, 2], [6, 1], [7, 8]])); // 21
