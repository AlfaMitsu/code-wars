Large Factorials

    function factorial(n) {
      if (n < 0) {
        return null;
      }
    
      let result = '1';
      for (let i = 2; i <= n; i++) {
        result = multiply(result, i.toString());
      }
    
      return result;
    }
    
    function multiply(a, b) {
      let result = '0';
      for (let i = '0'; compare(i, b) < 0; i = add(i, '1')) {
        result = add(result, a);
      }
      return result;
    }
    
    function add(a, b) {
      let carry = 0;
      let result = '';
      let maxLength = Math.max(a.length, b.length);
      for (let i = 0; i < maxLength || carry; i++) {
        let sum = carry + (+(a[a.length - 1 - i] || 0)) + (+(b[b.length - 1 - i] || 0));
        carry = sum >= 10 ? 1 : 0;
        result = (sum % 10) + result;
      }
      return result;
    }
    
    function compare(a, b) {
      if (a.length !== b.length) {
        return a.length - b.length;
      }
      for (let i = 0; i < a.length; i++) {
        if (a[i] !== b[i]) {
          return a[i] - b[i];
        }
      }
      return 0;
    }
    
    // Test cases
    console.log(factorial(5)); // Output: "120"
    console.log(factorial(25)); // Output: "15511210043330985984000000"
    console.log(factorial(-1)); // Output: null
