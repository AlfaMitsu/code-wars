Sum without highest and lowest number

    function sumArray(array) {
      // Input validation: if the array is null, empty, or has only one element, return 0
      if (!array || array.length <= 1) {
        return 0;
      }
      
      // Find the highest and lowest values in the array
      let max = Math.max(...array);
      let min = Math.min(...array);
      
      // Calculate the sum of all elements in the array
      let totalSum = array.reduce((sum, num) => sum + num, 0);
      
      // Subtract the highest and lowest values from the total sum
      return totalSum - max - min;
    }
    
    // Example usage:
    console.log(sumArray([6, 2, 1, 8, 10])); // 16
    console.log(sumArray([1, 1, 11, 2, 3])); // 6
    console.log(sumArray(null)); // 0
    console.log(sumArray([])); // 0
    console.log(sumArray([1])); // 0
    console.log(sumArray([1, 1])); // 0
