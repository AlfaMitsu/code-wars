Sum of Minimums

    function sumOfMinimums(arr) {
      let sum = 0;
      for (let i = 0; i < arr.length; i++) {
        let min = Math.min(...arr[i]);
        sum += min;
      }
      return sum;
    }
    
    // Test the function
    console.log(sumOfMinimums([
      [1, 2, 3, 4, 5],
      [5, 6, 7, 8, 9],
      [20, 21, 34, 56, 100]
    ])); // Output: 26
