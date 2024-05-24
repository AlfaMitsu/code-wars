Calculate Average

    function findAverage(array) {
      // Check if the array is empty
      if (array.length === 0) {
        return 0;
      }
      
      // Calculate the sum of the numbers in the array
      let sum = array.reduce((acc, num) => acc + num, 0);
      
      // Calculate the average
      return sum / array.length;
    }
    
    // Examples
    console.log(findAverage([1, 2, 3, 4, 5])); // 3
    console.log(findAverage([10, 20, 30, 40, 50])); // 30
    console.log(findAverage([])); // 0
