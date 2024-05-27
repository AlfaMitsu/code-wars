Filter out the Geese

    function gooseFilter(birds) {
      var geese = ["African", "Roman Tufted", "Toulouse", "Pilgrim", "Steinbacher"];
      
      // Use the filter method to exclude geese from the birds array
      return birds.filter(bird => !geese.includes(bird));
    }
    
    // Example usage:
    console.log(gooseFilter(["Mallard", "Hook Bill", "African", "Crested", "Pilgrim", "Toulouse", "Blue Swedish"])); 
    // Output: ["Mallard", "Hook Bill", "Crested", "Blue Swedish"]
