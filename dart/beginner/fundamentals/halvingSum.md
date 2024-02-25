Halving Sum

    int halvingSum(int n) {
      int sum = 0;
      while (n > 0) {
        sum += n;
        n ~/= 2;
      }
      return sum;
    }
