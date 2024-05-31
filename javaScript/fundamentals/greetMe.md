Greet Me

    var greet = function(name) {
        // Capitalize the first letter of the name
        var capitalized = name.charAt(0).toUpperCase() + name.slice(1).toLowerCase();
    
        // Return the greeting
        return "Hello " + capitalized + "!";
    };
    
    // Test cases
    console.log(greet("riley")); // Should return "Hello Riley!"
    console.log(greet("JACK"));  // Should return "Hello Jack!"
