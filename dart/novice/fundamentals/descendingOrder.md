Descending Order

    int descendingOrder(int n) {
      List<int> digits = n.toString().split('').map(int.parse).toList();
      digits.sort((a, b) => b.compareTo(a));
      return int.parse(digits.join(''));
    }
