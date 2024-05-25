All Star Code Challenge #18

    function strCount(str, letter) {
      let count = 0;
      for (let i = 0; i < str.length; i++) {
        if (str[i] === letter) {
          count++;
        }
      }
      return count;
    }
    
    // Test cases
    console.log(strCount("Hello", "o")); // Output: 1
    console.log(strCount("Hello", "l")); // Output: 2
    console.log(strCount("", "z"));      // Output: 0
