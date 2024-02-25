Number in Strings

    int solve(String s) {
      int largestNumber = 0;
      int currentNumber = 0;
    
      for (int i = 0; i < s.length; i++) {
        if (s[i].contains(RegExp(r'\d'))) {
          currentNumber = currentNumber * 10 + int.parse(s[i]);
        } else {
          largestNumber = currentNumber > largestNumber ? currentNumber : largestNumber;
          currentNumber = 0;
        }
      }
    
      // Check the last number group
      largestNumber = currentNumber > largestNumber ? currentNumber : largestNumber;
    
      return largestNumber;
    }
