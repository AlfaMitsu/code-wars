Are Arrow Function Odd?

    function odds(values){
      return values.filter(value => value % 2 !== 0);
    }
    
    // Test cases
    console.log(odds([1, 2, 3, 4, 5]));  // Output: [1, 3, 5]
    console.log(odds([2, 4, 6]));         // Output: []
