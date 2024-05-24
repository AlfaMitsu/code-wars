Pete the Baker

    function cakes(recipe, available) {
      let maxCakes = Infinity;
      for (let ingredient in recipe) {
        if (!(ingredient in available)) {
          return 0; // If any required ingredient is missing, no cakes can be made
        }
        maxCakes = Math.min(maxCakes, Math.floor(available[ingredient] / recipe[ingredient]));
      }
      return maxCakes;
    }
    
    // Example usage
    console.log(cakes({flour: 500, sugar: 200, eggs: 1}, {flour: 1200, sugar: 1200, eggs: 5, milk: 200})); // Output: 2
    console.log(cakes({apples: 3, flour: 300, sugar: 150, milk: 100, oil: 100}, {sugar: 500, flour: 2000, milk: 2000})); // Output: 0
