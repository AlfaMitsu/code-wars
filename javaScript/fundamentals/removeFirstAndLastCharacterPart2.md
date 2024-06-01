Remove first and last character part 2

    function array(string) {
      // Split the input string by commas
      let arr = string.split(',');
      
      // Remove the first and last elements
      arr = arr.slice(1, -1);
      
      // Join the remaining elements with spaces
      let result = arr.join(' ');
      
      // Return NULL if the result is empty, otherwise return the result
      return result === '' ? null : result;
    }
    
    // Test cases
    console.log(array("1,2,3"));      // "2"
    console.log(array("1,2,3,4"));    // "2 3"
    console.log(array("1,2,3,4,5"));  // "2 3 4"
    console.log(array(""));           // null
    console.log(array("1"));          // null
    console.log(array("1,2"));        // null
