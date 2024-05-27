Remove Anchor from URL

    function removeUrlAnchor(url) {
      // Find the index of the '#' character
      const anchorIndex = url.indexOf('#');
      
      // If '#' is found, return the substring before it, otherwise return the original URL
      return anchorIndex !== -1 ? url.slice(0, anchorIndex) : url;
    }
    
    // Example usage:
    console.log(removeUrlAnchor("www.codewars.com#about")); // "www.codewars.com"
    console.log(removeUrlAnchor("www.codewars.com?page=1")); // "www.codewars.com?page=1"
