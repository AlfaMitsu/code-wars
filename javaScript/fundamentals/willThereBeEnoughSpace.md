Will there be enough space?

    function enough(cap, on, wait) {
      // Calculate the total number of people if all waiting passengers get on
      const total = on + wait;
      
      // If the total is less than or equal to the capacity, return 0
      if (total <= cap) {
        return 0;
      }
      
      // Otherwise, return the number of passengers that can't fit
      return total - cap;
    }
    
    // Example usage:
    console.log(enough(10, 5, 5)); // 0
    console.log(enough(100, 60, 50)); // 10
    console.log(enough(20, 5, 15)); // 0
    console.log(enough(10, 5, 6)); // 1
    console.log(enough(50, 30, 25)); // 5
