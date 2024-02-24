Sum of Positive

    int positiveSum(List<int> arr) {
      return arr.where((num) => num > 0).fold(0, (prev, curr) => prev + curr);
    }
