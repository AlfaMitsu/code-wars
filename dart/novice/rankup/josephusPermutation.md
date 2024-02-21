Josephus Permutation

    List<T> josephus<T>(final List<T> items, final int k) {
      List<T> result = [];
      int index = 0;
      while (items.isNotEmpty) {
        index = (index + k - 1) % items.length;
        result.add(items.removeAt(index));
      }
      return result;
    }
