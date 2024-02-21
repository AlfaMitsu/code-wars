Odd Ones Out!

    List<int> oddOnesOut(List<int> nums) {
      Map<int, int> counts = {};
      for (int num in nums) {
        counts[num] = (counts[num] ?? 0) + 1;
      }
      
      List<int> result = [];
      for (int num in nums) {
        if (counts[num]! % 2 == 0) {
          result.add(num);
        }
      }
      
      return result;
    }
