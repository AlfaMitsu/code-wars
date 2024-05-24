Find the unique number

    function findUniq(arr) {
      // Sort the array to bring the potential unique number to either the first or last position
      arr.sort((a, b) => a - b);
    
      // Check if the unique number is at the first or last position
      if (arr[0] !== arr[1]) {
        return arr[0];
      } else {
        return arr[arr.length - 1];
      }
    }
    
    // Example usage
    console.log(findUniq([1, 1, 1, 2, 1, 1])); // Output: 2
    console.log(findUniq([0, 0, 0.55, 0, 0])); // Output: 0.55
