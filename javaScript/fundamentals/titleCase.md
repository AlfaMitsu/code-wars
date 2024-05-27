Title Case

    function titleCase(title, minorWords) {
      if (!title) return '';
    
      // Convert the minor words string to an array of lowercase words
      let minorWordsArray = minorWords ? minorWords.toLowerCase().split(' ') : [];
    
      // Split the title string into an array of words
      let words = title.toLowerCase().split(' ');
    
      // Iterate through each word in the title
      let result = words.map((word, index) => {
        // Capitalize the first word or words not in the minorWords array
        if (index === 0 || !minorWordsArray.includes(word)) {
          return word.charAt(0).toUpperCase() + word.slice(1);
        } else {
          // Otherwise, return the word in lowercase
          return word;
        }
      });
    
      // Join the processed words back into a single string
      return result.join(' ');
    }
    
    // Example usage:
    console.log(titleCase('a clash of KINGS', 'a an the of')); // 'A Clash of Kings'
    console.log(titleCase('THE WIND IN THE WILLOWS', 'The In')); // 'The Wind in the Willows'
    console.log(titleCase('the quick brown fox')); // 'The Quick Brown Fox'
