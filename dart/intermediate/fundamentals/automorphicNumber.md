Automorphic Number

    String automorphic(int n) {
      int square = n * n;
      String squareStr = square.toString();
      String nStr = n.toString();
      return squareStr.endsWith(nStr) ? "Automorphic" : "Not!!";
    }
