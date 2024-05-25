Next bigger number with the same digits

    function nextBigger(n) {
      const digits = String(n).split('').map(Number);
    
      let pivotIndex = -1;
      for (let i = digits.length - 2; i >= 0; i--) {
        if (digits[i] < digits[i + 1]) {
          pivotIndex = i;
          break;
        }
      }
    
      if (pivotIndex === -1) return -1;
    
      let swapIndex = pivotIndex + 1;
      for (let i = pivotIndex + 2; i < digits.length; i++) {
        if (digits[i] > digits[pivotIndex] && digits[i] < digits[swapIndex]) {
          swapIndex = i;
        }
      }
    
      [digits[pivotIndex], digits[swapIndex]] = [digits[swapIndex], digits[pivotIndex]];
      const sortedTail = digits.splice(pivotIndex + 1).sort((a, b) => a - b);
      digits.push(...sortedTail);
    
      const nextBiggerNumber = Number(digits.join(''));
      return nextBiggerNumber > n ? nextBiggerNumber : -1;
    }
    
    // Test cases
    console.log(nextBigger(12));    // Output: 21
    console.log(nextBigger(513));   // Output: 531
    console.log(nextBigger(2017));  // Output: 2071
    console.log(nextBigger(9));     // Output: -1
    console.log(nextBigger(111));   // Output: -1
    console.log(nextBigger(531));   // Output: -1
