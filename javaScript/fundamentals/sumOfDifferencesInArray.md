Sum of differences in array

    function sumOfDifferences(arr) {
        arr.sort((a, b) => b - a); // Sort array in descending order
        let sum = 0;
        for (let i = 0; i < arr.length - 1; i++) {
            sum += arr[i] - arr[i + 1]; // Calculate difference between consecutive pairs
        }
        return sum;
    }
