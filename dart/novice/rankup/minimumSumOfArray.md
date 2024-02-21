Minimum Sum of Array

    int minSum(List<int> arr) {
      arr.sort();
      int sum = 0;
      for (int i = 0; i < arr.length / 2; i++) {
        sum += arr[i] * arr[arr.length - 1 - i];
      }
      return sum;
    }
