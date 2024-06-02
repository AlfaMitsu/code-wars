Find the position

    function position(letter) {
      // Get the ASCII code of the letter and subtract the ASCII code of 'a'
      // Then add 1 to get the position in the alphabet
      const position = letter.charCodeAt(0) - 'a'.charCodeAt(0) + 1;
      
      // Return the position in the required format
      return `Position of alphabet: ${position}`;
    }
    
    // Example usage:
    console.log(position("a")); // Output: "Position of alphabet: 1"
    console.log(position("z")); // Output: "Position of alphabet: 26"
    console.log(position("m")); // Output: "Position of alphabet: 13"
