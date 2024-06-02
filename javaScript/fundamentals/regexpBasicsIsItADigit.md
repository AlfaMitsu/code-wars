Regexp Basics - is it a digit?

    String.prototype.digit = function() {
      // Check if the string matches a single digit from 0 to 9
      return /^\d$/.test(this);
    };
    
    // Example usage:
    console.log("5".digit()); // Output: true
    console.log("a".digit()); // Output: false
    console.log("10".digit()); // Output: false
