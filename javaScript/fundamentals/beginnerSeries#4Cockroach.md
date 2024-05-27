Beginner Series #4: Cockroach

    function cockroachSpeed(s) {
      // Convert km/h to cm/s and floor the result
      return Math.floor(s * 100000 / 3600);
    }
    
    // Example usage:
    console.log(cockroachSpeed(1.08)); // 30
    console.log(cockroachSpeed(1.5)); // 41
    console.log(cockroachSpeed(0)); // 0
