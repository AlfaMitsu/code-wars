Simple validation of a Username with Regex

    function validateUsr(username) {
      const res = /^[a-z0-9_]{4,16}$/.test(username);
      return res;
    }
    
    // Example usage:
    console.log(validateUsr("valid_user1")); // true
    console.log(validateUsr("InvalidUser")); // false (contains uppercase letters)
    console.log(validateUsr("user!"));       // false (contains invalid character '!')
    console.log(validateUsr("usr"));         // false (too short)
    console.log(validateUsr("valid_user_1234567890")); // false (too long)
