Sum of two lowest positive integers

    function sumTwoSmallestNumbers(numbers) {  
      // Sort the array in ascending order
      numbers.sort((a, b) => a - b);
      
      // Sum the first two elements
      return numbers[0] + numbers[1];
    }
    
    // Examples
    console.log(sumTwoSmallestNumbers([19, 5, 42, 2, 77])); // 7
    console.log(sumTwoSmallestNumbers([10, 343445353, 3453445, 3453545353453])); // 3453455
    console.log(sumTwoSmallestNumbers([3, 8, 15, 1])); // 4
    console.log(sumTwoSmallestNumbers([23, 71, 33, 82, 1])); // 24
