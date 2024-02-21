Tribonacci Sequence

    List<num> tribonacci(List<num> signature, int n) {
      List<num> result = [];
      if (n == 0) return result;
      
      result.addAll(signature);
      while (result.length < n) {
        result.add(result[result.length - 1] + result[result.length - 2] + result[result.length - 3]);
      }
    
      return result.sublist(0, n);
    }
