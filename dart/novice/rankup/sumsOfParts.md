Sum of Parts

    List<int> partsSums(List<int> ls) {
      List<int> sums = [];
      int sum = ls.fold(0, (a, b) => a + b);
      sums.add(sum);
      for (int i = 0; i < ls.length; i++) {
        sum -= ls[i];
        sums.add(sum);
      }
      return sums;
    }
