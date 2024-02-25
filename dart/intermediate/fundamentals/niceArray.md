Nice Array

    bool isNice(List<int> arr) {
      if (arr.isEmpty) return false;
    
      for (var n in arr) {
        if (!arr.contains(n - 1) && !arr.contains(n + 1)) {
          return false;
        }
      }
    
      return true;
    }
