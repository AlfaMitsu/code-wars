Fibonacci, Tribonacci and friends

    function Xbonacci(signature, n) {
      let result = signature.slice(0, n); // Initialize result with signature elements, up to n elements if n < signature length
    
      while (result.length < n) {
        let nextElement = result.slice(-signature.length).reduce((a, b) => a + b, 0); // Sum of the last 'signature.length' elements
        result.push(nextElement); // Add the new element to the sequence
      }
    
      return result;
    }
    
    // Example usage:
    console.log(Xbonacci([1, 1, 1, 1], 10)); // Outputs: [1, 1, 1, 1, 4, 7, 13, 25, 49, 94]
    console.log(Xbonacci([0, 0, 0, 0, 1], 10)); // Outputs: [0, 0, 0, 0, 1, 1, 2, 4, 8, 16]
    console.log(Xbonacci([1, 0, 0, 0, 0, 0, 1], 10)); // Outputs: [1, 0, 0, 0, 0, 0, 1, 2, 3, 6]
    console.log(Xbonacci([1, 1], 10)); // Outputs: [1, 1, 2, 3, 5, 8, 13, 21, 34, 55]
