Replace with Alphabet Position

    function alphabetPosition(text) {
      let result = "";
      for (let i = 0; i < text.length; i++) {
        let charCode = text.toUpperCase().charCodeAt(i);
        if (charCode >= 65 && charCode <= 90) {
          result += (charCode - 64) + " ";
        }
      }
      return result.trim();
    }
    
    // Test case
    let input = "The sunset sets at twelve o' clock.";
    console.log(alphabetPosition(input));
