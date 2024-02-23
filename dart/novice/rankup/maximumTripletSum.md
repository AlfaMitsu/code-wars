Maximum Triplet Sum

    int maxTriSum(List<int> nums) {
      Set<int> uniqueNumbers = nums.toSet();
      List<int> uniqueList = uniqueNumbers.toList();
      uniqueList.sort((a, b) => b - a); // Sort in descending order
      int sum = 0;
      for (int i = 0; i < 3 && i < uniqueList.length; i++) {
        sum += uniqueList[i];
      }
      return sum;
    }
