Factorial

    function factorial(n) {
      if (n < 0 || n > 12) {
        throw new RangeError("Input must be between 0 and 12");
      }
      if (n === 0) {
        return 1;
      }
      return n * factorial(n - 1);
    }
    
    // Example usage
    try {
      console.log(factorial(5)); // Output: 120
      console.log(factorial(0)); // Output: 1
      console.log(factorial(13)); // Throws RangeError
    } catch (error) {
      console.error(error.message);
    }
