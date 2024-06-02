Extract the domain name from a URL

    function domainName(url){
      // Remove protocol (http, https, ftp, etc.)
      url = url.replace(/^(?:https?:\/\/)?(?:www\.)?/, "");
    
      // Extract the domain name before the next '/' or end of string
      return url.split('.')[0];
    }
    
    // Example usage:
    console.log(domainName("http://github.com/carbonfive/raygun")); // Output: "github"
    console.log(domainName("http://www.zombie-bites.com"));         // Output: "zombie-bites"
    console.log(domainName("https://www.cnet.com"));                // Output: "cnet"
