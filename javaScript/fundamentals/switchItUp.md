Switch It Up

    function switchItUp(number) {
      // Use a switch statement to map numbers to words
      switch (number) {
        case 0:
          return "Zero";
        case 1:
          return "One";
        case 2:
          return "Two";
        case 3:
          return "Three";
        case 4:
          return "Four";
        case 5:
          return "Five";
        case 6:
          return "Six";
        case 7:
          return "Seven";
        case 8:
          return "Eight";
        case 9:
          return "Nine";
        default:
          return "Invalid number"; // Optional: handle cases outside 0-9
      }
    }
    
    // Examples
    console.log(switchItUp(1)); // "One"
    console.log(switchItUp(0)); // "Zero"
    console.log(switchItUp(9)); // "Nine"
    console.log(switchItUp(5)); // "Five"
