Extra perfect numbers

    List<int> extraPerfect(int n) {
      List<int> result = [];
      for (int i = 1; i <= n; i += 2) {
        result.add(i);
      }
      return result;
    }
