Flatten and sort an array

    List<int> flattenAndSort(List<List<int>> arr) {
      return arr.expand((list) => list).toList()..sort();
    }
