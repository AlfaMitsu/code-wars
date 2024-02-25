Sort out the men from boys

    List<int> menFromBoys(List<int> arr) {
      List<int> even = arr.where((x) => x.isEven).toSet().toList()..sort();
      List<int> odd = arr.where((x) => x.isOdd).toSet().toList()..sort((a, b) => b.compareTo(a));
      return [...even, ...odd];
    }
