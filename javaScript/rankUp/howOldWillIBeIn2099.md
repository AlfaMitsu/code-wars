How old will be in 2099?

    function calculateAge(birthYear, targetYear) {
      const age = targetYear - birthYear;
    
      if (age > 0) {
        return `You are ${age} year${age > 1 ? 's' : ''} old.`;
      } else if (age < 0) {
        return `You will be born in ${-age} year${-age > 1 ? 's' : ''}.`;
      } else {
        return "You were born this very year!";
      }
    }
    
    // Examples
    console.log(calculateAge(2000, 2090)); // "You are 90 years old."
    console.log(calculateAge(2000, 1990)); // "You will be born in 10 years."
    console.log(calculateAge(2000, 2000)); // "You were born this very year!"
    console.log(calculateAge(2000, 2001)); // "You are 1 year old."
    console.log(calculateAge(2000, 1999)); // "You will be born in 1 year."
