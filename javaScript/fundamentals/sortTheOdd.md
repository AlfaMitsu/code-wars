Sort the Odd

    function sortArray(array) {
      // Extract odd numbers and sort them
      const sortedOdds = array.filter(n => n % 2 !== 0).sort((a, b) => a - b);
      
      // Iterate through the original array and replace odd numbers with sorted ones
      let oddIndex = 0;
      return array.map(n => (n % 2 !== 0 ? sortedOdds[oddIndex++] : n));
    }
    
    // Test cases
    console.log(sortArray([7, 1])); // [1, 7]
    console.log(sortArray([5, 8, 6, 3, 4])); // [3, 8, 6, 5, 4]
    console.log(sortArray([9, 8, 7, 6, 5, 4, 3, 2, 1, 0])); // [1, 8, 3, 6, 5, 4, 7, 2, 9, 0]
