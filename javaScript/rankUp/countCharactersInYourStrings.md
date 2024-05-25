Count characters in your strings

    function count(string) {
      let charCount = {};
      for (let char of string) {
        charCount[char] = (charCount[char] || 0) + 1;
      }
      return charCount;
    }
    
    // Test cases
    console.log(count("aba"));  // Output: { 'a': 2, 'b': 1 }
    console.log(count(""));     // Output: {}
