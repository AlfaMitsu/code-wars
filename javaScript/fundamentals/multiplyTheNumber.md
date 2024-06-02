Multiply the number

    function multiply(number) {
      // Get the absolute value of the number and convert it to a string
      const numStr = Math.abs(number).toString();
      
      // Count the number of digits
      const numDigits = numStr.length;
      
      // Calculate the power of 5
      const powerOfFive = Math.pow(5, numDigits);
      
      // Return the result of the multiplication
      return number * powerOfFive;
    }
    
    // Examples:
    console.log(multiply(3));    // Output: 15
    console.log(multiply(10));   // Output: 250
    console.log(multiply(200));  // Output: 25000
    console.log(multiply(0));    // Output: 0
    console.log(multiply(-3));   // Output: -15
