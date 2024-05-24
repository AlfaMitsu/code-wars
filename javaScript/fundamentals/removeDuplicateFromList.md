Remove Duplicate from list

    function distinct(a) {
      let result = [];
      let seen = new Set();
    
      for (let num of a) {
        if (!seen.has(num)) {
          result.push(num);
          seen.add(num);
        }
      }
    
      return result;
    }
    
    // Examples
    console.log(distinct([1, 1, 2])); // [1, 2]
    console.log(distinct([1, 2, 1, 1, 3, 2])); // [1, 2, 3]
