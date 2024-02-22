Pyramid Array

    List<List<int>> pyramid(int n) {
      List<List<int>> result = [];
      for (int i = 1; i <= n; i++) {
        result.add(List<int>.filled(i, 1));
      }
      return result;
    }
