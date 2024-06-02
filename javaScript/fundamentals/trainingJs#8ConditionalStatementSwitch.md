Training JS #8: Conditional statement--switch

    function howManydays(month) {
      var days;
      switch (month) {
        case 1:
        case 3:
        case 5:
        case 7:
        case 8:
        case 10:
        case 12:
          days = 31;
          break;
        case 4:
        case 6:
        case 9:
        case 11:
          days = 30;
          break;
        case 2:
          days = 28;
          break;
        default:
          days = 0; // Default case is optional since month is guaranteed to be 1-12
      }
      return days;
    }
