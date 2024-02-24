How much?

    List<List<String>> howmuch(int m, int n) {
      int start = m < n ? m : n;
      int end = m < n ? n : m;
      List<List<String>> result = [];
      for (int f = start; f <= end; f++) {
        if ((f - 1) % 9 == 0 && (f - 2) % 7 == 0) {
          int c = (f - 1) ~/ 9;
          int b = (f - 2) ~/ 7;
          result.add(["M: $f", "B: $b", "C: $c"]);
        }
      }
      return result;
    }
