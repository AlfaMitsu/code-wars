Sum Arrays

    function sum(numbers) {
        "use strict";
        let total = 0;
        for (let i = 0; i < numbers.length; i++) {
            total += numbers[i];
        }
        return total;
    }
    
    // Test cases
    console.log(sum([1, 5.2, 4, 0, -1]));  // Output: 9.2
    console.log(sum([]));                   // Output: 0
    console.log(sum([-2.398]));             // Output: -2.398
