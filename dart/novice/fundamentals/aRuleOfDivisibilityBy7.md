A rule of divisibility by 7

    List<int> seven(int m) {
      int steps = 0;
      while (m > 99) {
        m = m ~/ 10 - (m % 10) * 2;
        steps++;
      }
      return [m, steps];
    }
