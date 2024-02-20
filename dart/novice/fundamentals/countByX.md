Count by X

    List<int> countBy(int x, int n) {
      List<int> multiples = [];
      for (int i = 1; i <= n; i++) {
        multiples.add(x * i);
      }
      return multiples;
    }
