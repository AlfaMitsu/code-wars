Exclamation marks series #1: Remove an exclamation mark from the end of string

    function remove(string) {
      // Check if the last character is an exclamation mark
      if (string.endsWith('!')) {
        // Remove the last character
        return string.slice(0, -1);
      }
      // Return the original string if there's no exclamation mark at the end
      return string;
    }
    
    // Example usage:
    console.log(remove("Hi!")); // "Hi"
    console.log(remove("Hi!!!")); // "Hi!!"
    console.log(remove("!Hi")); // "!Hi"
    console.log(remove("!Hi!")); // "!Hi"
    console.log(remove("Hi! Hi!")); // "Hi! Hi"
    console.log(remove("Hi")); // "Hi"
