No zeroes for heroes

    function noBoringZeros(n) {
      // Convert the number to a string
      let numStr = n.toString();
      
      // Use a regular expression to remove trailing zeros
      numStr = numStr.replace(/0+$/, '');
    
      // Convert the string back to a number and return
      return Number(numStr);
    }
    
    // Example usage:
    console.log(noBoringZeros(1450)); // 145
    console.log(noBoringZeros(960000)); // 96
    console.log(noBoringZeros(1050)); // 105
    console.log(noBoringZeros(-1050)); // -105
    console.log(noBoringZeros(0)); // 0
