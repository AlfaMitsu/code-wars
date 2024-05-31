No Oddities here

    function noOdds(values) {
      // Use the filter method to return only non-odd (even) values
      return values.filter(value => value % 2 === 0);
    }
    
    // Examples
    console.log(noOdds([1, 2, 3, 4, 5, 6])); // [2, 4, 6]
    console.log(noOdds([11, 13, 15, 20, 22])); // [20, 22]
    console.log(noOdds([0, -2, -3, -4])); // [0, -2, -4]
    console.log(noOdds([7, 9, 11])); // []
