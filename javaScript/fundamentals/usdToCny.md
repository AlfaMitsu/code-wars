USD to CNY

    function usdcny(usd) {
        // Calculate the amount in CNY
        let cny = (usd * 6.75).toFixed(2);
    
        // Return the formatted string
        return cny + ' Chinese Yuan';
    }
    
    // Test cases
    console.log(usdcny(15));  // Should return '101.25 Chinese Yuan'
    console.log(usdcny(465)); // Should return '3138.75 Chinese Yuan'
