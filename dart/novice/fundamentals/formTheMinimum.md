Form the Minimum

    int minValue(List<int> arr) {
      List<int> uniqueDigits = arr.toSet().toList();
      uniqueDigits.sort();
      int result = 0;
      for (int digit in uniqueDigits) {
        result = result * 10 + digit;
      }
      return result;
    }
