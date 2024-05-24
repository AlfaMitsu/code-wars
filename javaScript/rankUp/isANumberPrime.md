Is a number Prime?

    function isPrime(num) {
      if (num <= 1) {
        return false;
      }
      if (num === 2) {
        return true;
      }
      if (num % 2 === 0) {
        return false;
      }
    
      for (let i = 3; i <= Math.sqrt(num); i += 2) {
        if (num % i === 0) {
          return false;
        }
      }
    
      return true;
    }
    
    // Examples
    console.log(isPrime(1));   // false
    console.log(isPrime(2));   // true
    console.log(isPrime(-1));  // false
