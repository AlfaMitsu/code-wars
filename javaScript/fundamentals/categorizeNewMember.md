Categorize New Member

    function openOrSenior(data) {
      // Initialize the result array
      let result = [];
    
      // Iterate through each pair of age and handicap
      for (let i = 0; i < data.length; i++) {
        let [age, handicap] = data[i];
    
        // Apply the criteria to determine the category
        if (age >= 55 && handicap > 7) {
          result.push("Senior");
        } else {
          result.push("Open");
        }
      }
    
      // Return the result array
      return result;
    }
    
    // Example usage:
    let input = [[18, 20], [45, 2], [61, 12], [37, 6], [21, 21], [78, 9]];
    console.log(openOrSenior(input)); // ["Open", "Open", "Senior", "Open", "Open", "Senior"]
