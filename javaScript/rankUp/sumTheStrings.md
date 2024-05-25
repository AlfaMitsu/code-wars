Sum the Strings

    function sumStr(a, b) {
      // Convert empty strings to "0"
      a = a || "0";
      b = b || "0";
      // Convert strings to integers and sum them
      let sum = parseInt(a) + parseInt(b);
      // Convert sum back to a string and return
      return sum.toString();
    }
    
    // Test cases
    console.log(sumStr("4", "5"));   // Output: "9"
    console.log(sumStr("34", "5"));  // Output: "39"
    console.log(sumStr("", ""));     // Output: "0"
    console.log(sumStr("2", ""));    // Output: "2"
    console.log(sumStr("-5", "3"));  // Output: "-2"
