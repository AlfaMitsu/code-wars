Remove Exclamation Marks

    function removeExclamationMarks(s) {
      return s.replace(/!/g, '');
    }
    
    // Test cases
    console.log(removeExclamationMarks("Hello!")); // "Hello"
    console.log(removeExclamationMarks("Hello World!!!")); // "Hello World"
    console.log(removeExclamationMarks("!Hi! There!")); // "Hi There"
    console.log(removeExclamationMarks("No exclamations here.")); // "No exclamations here."
