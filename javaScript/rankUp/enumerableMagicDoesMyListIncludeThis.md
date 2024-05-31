Enumerable Magic - Does My List Include This?

    function include(arr, item) {
      return arr.includes(item);
    }
    
    // Example usages
    console.log(include([1, 2, 3, 4], 3));  // Output: true
    console.log(include([1, 2, 3, 4], 5));  // Output: false
    console.log(include(['a', 'b', 'c'], 'b'));  // Output: true
    console.log(include(['a', 'b', 'c'], 'd'));  // Output: false
