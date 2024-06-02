Is there a vowel in there?

    function isVow(a) {
      // Define the character codes for lowercase vowels
      const vowels = {
        97: 'a',  // 'a' character code
        101: 'e', // 'e' character code
        105: 'i', // 'i' character code
        111: 'o', // 'o' character code
        117: 'u'  // 'u' character code
      };
    
      // Iterate through the array and replace numbers with corresponding vowels
      for (let i = 0; i < a.length; i++) {
        if (vowels[a[i]]) {
          a[i] = vowels[a[i]];
        }
      }
    
      return a;
    }
    
    // Example usage:
    console.log(isVow([97, 98, 99, 100, 101])); // ['a', 98, 99, 100, 'e']
    console.log(isVow([105, 106, 107, 108, 109, 111])); // ['i', 106, 107, 108, 109, 'o']
