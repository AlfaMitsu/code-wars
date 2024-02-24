Ones and Zeros

    int binaryArrayToNumber(List<int> arr) {
      int result = 0;
      for (int bit in arr) {
        result = result * 2 + bit;
      }
      return result;
    }
