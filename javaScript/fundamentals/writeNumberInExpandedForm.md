Write number in expanded form

    function expandedForm(num) {
        // Convert number to string
        let numStr = num.toString();
        let result = '';
    
        // Iterate through each digit
        for (let i = 0; i < numStr.length; i++) {
            // Check if the digit is not zero
            if (numStr[i] !== '0') {
                // Add the digit with appropriate number of zeros
                result += numStr[i] + '0'.repeat(numStr.length - i - 1) + ' + ';
            }
        }
    
        // Remove the extra ' + ' at the end and return the result
        return result.slice(0, -3);
    }
    
    // Test cases
    console.log(expandedForm(12));    // Should return '10 + 2'
    console.log(expandedForm(42));    // Should return '40 + 2'
    console.log(expandedForm(70304)); // Should return '70000 + 300 + 4'
