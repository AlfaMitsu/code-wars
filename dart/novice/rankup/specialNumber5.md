Special Number 5

    String specialNumber(int n) {
      String numStr = n.toString();
      for (int i = 0; i < numStr.length; i++) {
        int digit = int.parse(numStr[i]);
        if (digit < 0 || digit > 5) {
          return "NOT!!";
        }
      }
      return "Special!!";
    }
