Will you make it?

    const zeroFuel = (distanceToPump, mpg, fuelLeft) => {
      // Calculate the maximum distance the car can travel
      const maxDistance = mpg * fuelLeft;
      
      // Return true if the max distance is greater than or equal to the distance to the pump
      return maxDistance >= distanceToPump;
    }
    
    // Example usage:
    console.log(zeroFuel(50, 25, 2)); // true
    console.log(zeroFuel(100, 25, 3)); // false
    console.log(zeroFuel(60, 30, 2)); // true
    console.log(zeroFuel(10, 1, 10)); // true
    console.log(zeroFuel(200, 25, 7)); // false
