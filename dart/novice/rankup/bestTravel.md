Best Travel

    int chooseBestSum(int t, int k, List<int> ls) {
      if (ls.length < k) return -1;
    
      int? bestSum = null;
    
      void generateCombinations(int start, int count, int currentSum) {
        if (count == k) {
          if (currentSum <= t && (bestSum == null || currentSum > bestSum!)) {
            bestSum = currentSum;
          }
          return;
        }
    
        for (int i = start; i < ls.length; i++) {
          generateCombinations(i + 1, count + 1, currentSum + ls[i]);
        }
      }
    
      generateCombinations(0, 0, 0);
      return bestSum ?? -1;
    }
