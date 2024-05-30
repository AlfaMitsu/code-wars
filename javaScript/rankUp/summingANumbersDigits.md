Summing a numbers digits

    function sumDigits(number) {
      // Convert the number to its absolute value
      number = Math.abs(number);
    
      // Convert the number to a string and split into individual digits
      let digits = number.toString().split('');
    
      // Sum up the digits
      let sum = digits.reduce((acc, digit) => acc + parseInt(digit), 0);
    
      return sum;
    }
    
    // Example usages
    console.log(sumDigits(10));   // Output: 1
    console.log(sumDigits(99));   // Output: 18
    console.log(sumDigits(-32));  // Output: 5
