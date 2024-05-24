Reverse words in a String

    function reverse(string) {
      // Split the string into words, filter out any empty strings, reverse the array, and join it back into a string
      return string
        .split(' ')
        .filter(word => word.length > 0)
        .reverse()
        .join(' ');
    }
    
    // Examples
    console.log(reverse("Hello World")); // "World Hello"
    console.log(reverse("Hi There."));   // "There. Hi"
    console.log(reverse("  Hello   World  ")); // "World Hello"
    console.log(reverse("")); // ""
