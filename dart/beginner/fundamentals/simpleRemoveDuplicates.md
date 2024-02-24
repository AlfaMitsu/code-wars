Simple Remove Duplicates

    List<int> solve(List<int> arr) {
      var seen = <int>{};
      return arr.reversed.where((element) => seen.add(element)).toList().reversed.toList();
    }
