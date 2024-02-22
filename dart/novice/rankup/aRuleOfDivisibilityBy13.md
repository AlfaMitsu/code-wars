A Rule of Divisibility by 13

    int thirt(int n) {
      List<int> pattern = [1, 10, 9, 12, 3, 4];
      List<int> digits = n.toString().split('').map((e) => int.parse(e)).toList();
      int sum = n;
      while (true) {
        int newSum = 0;
        for (int i = 0; i < digits.length; i++) {
          newSum += digits[digits.length - i - 1] * pattern[i % 6];
        }
        if (newSum == sum) {
          return newSum;
        }
        sum = newSum;
        digits = sum.toString().split('').map((e) => int.parse(e)).toList();
      }
    }
