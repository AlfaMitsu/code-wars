Mean Square Error

    var solution = function(firstArray, secondArray) {
      if (firstArray.length !== secondArray.length) {
        throw new Error('Arrays must be of equal length');
      }
    
      let sum = 0;
      for (let i = 0; i < firstArray.length; i++) {
        const diff = Math.abs(firstArray[i] - secondArray[i]);
        sum += diff * diff;
      }
    
      return sum / firstArray.length;
    };
    
    // Test cases
    console.log(solution([1, 2, 3], [4, 5, 6]));             // 9
    console.log(solution([10, 20, 10, 2], [10, 25, 5, -2])); // 16.5
    console.log(solution([-1, 0], [0, -1]));                 // 1
