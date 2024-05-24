Correct the mistakes of the character recognition software

    function correct(string) {
      return string.replace(/5/g, 'S')
                   .replace(/0/g, 'O')
                   .replace(/1/g, 'I');
    }
    
    // Examples
    console.log(correct("H3LL0")); // "HELLO"
    console.log(correct("1 L0VE PR0GRAMM1NG")); // "I LOVE PROGRAMMING"
    console.log(correct("MY NAME 15 JOHN")); // "MY NAME IS JOHN"
