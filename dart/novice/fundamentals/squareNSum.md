Square(n) Sum

    int squareSum(List numbers) {
      if (numbers.isEmpty) return 0;
      return numbers.map((number) => number * number).reduce((a, b) => a + b);
    }
