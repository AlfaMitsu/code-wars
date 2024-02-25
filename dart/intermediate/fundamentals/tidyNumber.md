Tidy Number

    bool tidyNumber(int n) {
      List<int> digits = n.toString().split('').map(int.parse).toList();
      for (int i = 0; i < digits.length - 1; i++) {
        if (digits[i] > digits[i + 1]) {
          return false;
        }
      }
      return true;
    }
