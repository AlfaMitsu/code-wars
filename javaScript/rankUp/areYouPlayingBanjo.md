Are you playing Banjo?

    function areYouPlayingBanjo(name) {
      // Check if the first letter (lowercase) is 'r'
      if (name[0].toLowerCase() === 'r') {
        return name + " plays banjo";
      } else {
        return name + " does not play banjo";
      }
    }
    
    // Test cases
    console.log(areYouPlayingBanjo("John")); // Output: John does not play banjo
    console.log(areYouPlayingBanjo("Rick"));  // Output: Rick plays banjo
