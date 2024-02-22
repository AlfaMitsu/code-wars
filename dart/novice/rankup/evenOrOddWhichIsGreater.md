Even or Odd - Which is Greater?

    String evenOrOdd(String str) {
      int evenSum = 0;
      int oddSum = 0;
    
      for (int i = 0; i < str.length; i++) {
        int digit = int.parse(str[i]);
        if (digit % 2 == 0) {
          evenSum += digit;
        } else {
          oddSum += digit;
        }
      }
    
      if (evenSum > oddSum) {
        return "Even is greater than Odd";
      } else if (oddSum > evenSum) {
        return "Odd is greater than Even";
      } else {
        return "Even and Odd are the same";
      }
    }
