A needle in the Haystack

    function findNeedle(haystack) {
      // Find the index of "needle" in the array
      const index = haystack.indexOf("needle");
      
      // Return the formatted message
      return `found the needle at position ${index}`;
    }
    
    // Test example
    console.log(findNeedle(["hay", "junk", "hay", "hay", "moreJunk", "needle", "randomJunk"])); // "found the needle at position 5"
