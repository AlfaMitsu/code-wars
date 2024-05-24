Break Camelcase

    function solution(string) {
      return string.replace(/[A-Z]/g, match => ' ' + match);
    }
    
    // Examples
    console.log(solution("camelCasing")); // "camel Casing"
    console.log(solution("identifier")); // "identifier"
    console.log(solution("")); // ""
