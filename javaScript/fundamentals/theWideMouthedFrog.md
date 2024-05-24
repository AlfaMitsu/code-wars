The Wide-Mouthed Frog

    function mouthSize(animal) {
      // Convert the animal name to lowercase
      const lowerCaseAnimal = animal.toLowerCase();
      
      // Check if the animal is an alligator and return the appropriate mouth size
      if (lowerCaseAnimal === "alligator") {
        return "small";
      } else {
        return "wide";
      }
    }
    
    // Examples
    console.log(mouthSize("alligator")); // "small"
    console.log(mouthSize("ALLIGATOR")); // "small"
    console.log(mouthSize("Alligator")); // "small"
    console.log(mouthSize("lion"));      // "wide"
    console.log(mouthSize("frog"));      // "wide"
