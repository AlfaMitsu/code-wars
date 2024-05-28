Lario and Muigi Pipe Problem

    function pipeFix(numbers) {
      // Find the minimum and maximum values in the input array
      const min = Math.min(...numbers);
      const max = Math.max(...numbers);
      
      // Create a new array with values from min to max (inclusive)
      const fixedPipes = [];
      for (let i = min; i <= max; i++) {
        fixedPipes.push(i);
      }
      
      return fixedPipes;
    }
    
    // Test examples
    console.log(pipeFix([1, 3, 5, 6, 7, 8])); // [1, 2, 3, 4, 5, 6, 7, 8]
    console.log(pipeFix([6, 8, 10])); // [6, 7, 8, 9, 10]
    console.log(pipeFix([1, 2, 3])); // [1, 2, 3]
