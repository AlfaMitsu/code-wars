Largest pair sum in array

    function largestPairSum(numbers) {
      numbers.sort((a, b) => b - a); // Sort in descending order
      return numbers[0] + numbers[1]; // Sum of the first two elements
    }
