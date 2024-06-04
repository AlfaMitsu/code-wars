A strangle trip to the market

    function isLockNessMonster(s) {
      // Check if the string contains any of the phrases indicating the Loch Ness Monster
      return s.includes("tree fiddy") || s.includes("3.50") || s.includes("three fifty");
    }
    
    // Example usage:
    console.log(isLockNessMonster("Do you have any change? I need about tree fiddy.")); // true
    console.log(isLockNessMonster("Sure, I have 3.50 right here.")); // true
    console.log(isLockNessMonster("It's going to cost three fifty.")); // true
    console.log(isLockNessMonster("No mention of the Loch Ness Monster here.")); // false
