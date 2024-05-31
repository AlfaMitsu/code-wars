Super Duper Easy

    function problem(x) {
      // Check if the input is a string
      if (typeof x === 'string') {
        return "Error";
      }
    
      // Otherwise, multiply the value by 50 and add 6
      return x * 50 + 6;
    }
    
    // Example usages
    console.log(problem(2));      // Output: 106
    console.log(problem(10));     // Output: 506
    console.log(problem(-3));     // Output: -144
    console.log(problem('hello')); // Output: "Error"
    console.log(problem('5'));     // Output: "Error"
    console.log(problem(0));      // Output: 6
