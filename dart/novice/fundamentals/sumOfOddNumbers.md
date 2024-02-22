Sum of Odd Numbers

    int rowSumOddNumbers(int n) {
      int start = n * n - n + 1;
      return List.generate(n, (index) => start + index * 2).reduce((a, b) => a + b);
    }
