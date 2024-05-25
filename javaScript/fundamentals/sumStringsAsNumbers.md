Sum Strings as numbers

    function sumStrings(a, b) {
      let result = '';
      let carry = 0;
      let maxLength = Math.max(a.length, b.length);
    
      for (let i = 0; i < maxLength || carry; i++) {
        const digitA = +a[a.length - 1 - i] || 0;
        const digitB = +b[b.length - 1 - i] || 0;
        const sum = digitA + digitB + carry;
        result = `${sum % 10}${result}`;
        carry = sum > 9 ? 1 : 0;
      }
    
      return result.replace(/^0+/, '') || '0';
    }
    
    // Test cases
    console.log(sumStrings('1', '2')); // '3'
