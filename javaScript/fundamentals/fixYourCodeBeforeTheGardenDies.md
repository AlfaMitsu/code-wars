Fix your code before the Garden dies

    function rainAmount(mm) {
        if (mm < 40) {
            return "You need to give your plant " + (40 - mm) + "mm of water";
        } else {
            return "Your plant has had more than enough water for today!";
        }
    }
    
    // Test examples
    console.log(rainAmount(30)); // "You need to give your plant 10mm of water"
    console.log(rainAmount(40)); // "Your plant has had more than enough water for today!"
    console.log(rainAmount(50)); // "Your plant has had more than enough water for today!"
