Validate code with Simple Regex

    function validateCode(code) {
      return /^[1-3]/.test(code);
    }
    
    // Test cases
    console.log(validateCode(123)); // true
    console.log(validateCode(456)); // false
    console.log(validateCode(789)); // false
    console.log(validateCode(234)); // true
